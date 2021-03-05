---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 3759b5255794fcceb16018ecfc49bba362a03928
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012846"
---
# <span data-ttu-id="0a5ce-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0a5ce-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="0a5ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="0a5ce-103">Rimuove una particolare versione di API</span><span class="sxs-lookup"><span data-stu-id="0a5ce-103">Removes a particular API Release</span></span>

## <span data-ttu-id="0a5ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a5ce-104">SYNTAX</span></span>

### <span data-ttu-id="0a5ce-105">ByApiReleaseId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0a5ce-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a5ce-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0a5ce-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a5ce-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0a5ce-107">DESCRIPTION</span></span>

<span data-ttu-id="0a5ce-108">Il cmdlet **Remove-AzAzureRmApiManagementApiRelease** rimuove una versione API esistente.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="0a5ce-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a5ce-109">EXAMPLES</span></span>

### <span data-ttu-id="0a5ce-110">Esempio 1: Rimuovere una versione di API</span><span class="sxs-lookup"><span data-stu-id="0a5ce-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="0a5ce-111">Questo comando rimuove la versione di API con i valori ApiId e ReleaseId specificati.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="0a5ce-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a5ce-112">PARAMETERS</span></span>

### <span data-ttu-id="0a5ce-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0a5ce-113">-ApiId</span></span>
<span data-ttu-id="0a5ce-114">Identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-114">Identifier of the API.</span></span>
<span data-ttu-id="0a5ce-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-115">This parameter is required.</span></span>

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

### <span data-ttu-id="0a5ce-116">-Context</span><span class="sxs-lookup"><span data-stu-id="0a5ce-116">-Context</span></span>
<span data-ttu-id="0a5ce-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0a5ce-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0a5ce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a5ce-119">-DefaultProfile</span></span>
<span data-ttu-id="0a5ce-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a5ce-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0a5ce-121">-InputObject</span></span>
<span data-ttu-id="0a5ce-122">Istanza di PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="0a5ce-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-123">This parameter is required.</span></span>

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

### <span data-ttu-id="0a5ce-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a5ce-124">-PassThru</span></span>
<span data-ttu-id="0a5ce-125">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="0a5ce-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="0a5ce-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="0a5ce-127">-ReleaseId</span></span>
<span data-ttu-id="0a5ce-128">Identificatore della versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-128">Identifier of the API Release.</span></span>
<span data-ttu-id="0a5ce-129">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-129">This parameter is required.</span></span>

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

### <span data-ttu-id="0a5ce-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a5ce-130">-Confirm</span></span>
<span data-ttu-id="0a5ce-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a5ce-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a5ce-132">-WhatIf</span></span>
<span data-ttu-id="0a5ce-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a5ce-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a5ce-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a5ce-135">CommonParameters</span></span>
<span data-ttu-id="0a5ce-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a5ce-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0a5ce-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a5ce-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="0a5ce-138">INPUTS</span></span>

### <span data-ttu-id="0a5ce-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0a5ce-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0a5ce-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0a5ce-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="0a5ce-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0a5ce-141">System.String</span></span>

## <span data-ttu-id="0a5ce-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a5ce-142">OUTPUTS</span></span>

### <span data-ttu-id="0a5ce-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0a5ce-143">System.Boolean</span></span>

## <span data-ttu-id="0a5ce-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="0a5ce-144">NOTES</span></span>

## <span data-ttu-id="0a5ce-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a5ce-145">RELATED LINKS</span></span>

[<span data-ttu-id="0a5ce-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0a5ce-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="0a5ce-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0a5ce-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="0a5ce-148">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0a5ce-148">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)