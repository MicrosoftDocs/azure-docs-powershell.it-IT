---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 16c73a389e6602999272255534312928fc4a13f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978941"
---
# <span data-ttu-id="6ed24-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="6ed24-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="6ed24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ed24-102">SYNOPSIS</span></span>
<span data-ttu-id="6ed24-103">Aggiorna una specifica versione di Api.</span><span class="sxs-lookup"><span data-stu-id="6ed24-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="6ed24-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ed24-104">SYNTAX</span></span>

### <span data-ttu-id="6ed24-105">ExpandedParameter (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6ed24-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6ed24-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6ed24-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ed24-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6ed24-107">DESCRIPTION</span></span>
<span data-ttu-id="6ed24-108">Il cmdlet **Update-AzApiManagementApiRelease** modifica una versione dell'API Di gestione API di Azure.</span><span class="sxs-lookup"><span data-stu-id="6ed24-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="6ed24-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ed24-109">EXAMPLES</span></span>

### <span data-ttu-id="6ed24-110">Esempio 1: Aggiorna una versione di API per una revisione dell'API</span><span class="sxs-lookup"><span data-stu-id="6ed24-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="6ed24-111">Questo comando aggiorna la `echo-api-release` versione API dell'Api `echo-api` con una nuova nota.</span><span class="sxs-lookup"><span data-stu-id="6ed24-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="6ed24-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ed24-112">PARAMETERS</span></span>

### <span data-ttu-id="6ed24-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6ed24-113">-ApiId</span></span>
<span data-ttu-id="6ed24-114">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="6ed24-114">Identifier of existing API.</span></span>
<span data-ttu-id="6ed24-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6ed24-115">This parameter is required.</span></span>

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

### <span data-ttu-id="6ed24-116">-Context</span><span class="sxs-lookup"><span data-stu-id="6ed24-116">-Context</span></span>
<span data-ttu-id="6ed24-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6ed24-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6ed24-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6ed24-118">This parameter is required.</span></span>

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

### <span data-ttu-id="6ed24-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ed24-119">-DefaultProfile</span></span>
<span data-ttu-id="6ed24-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ed24-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ed24-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ed24-121">-InputObject</span></span>
<span data-ttu-id="6ed24-122">Istanza di tipo Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="6ed24-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ed24-123">-Nota</span><span class="sxs-lookup"><span data-stu-id="6ed24-123">-Note</span></span>
<span data-ttu-id="6ed24-124">Note sulla versione dell'Api.</span><span class="sxs-lookup"><span data-stu-id="6ed24-124">Api Release Notes.</span></span>
<span data-ttu-id="6ed24-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6ed24-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="6ed24-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ed24-126">-PassThru</span></span>
<span data-ttu-id="6ed24-127">Se si specifica l'istanza di Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease che rappresenta il rilascio API impostato.</span><span class="sxs-lookup"><span data-stu-id="6ed24-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="6ed24-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="6ed24-128">-ReleaseId</span></span>
<span data-ttu-id="6ed24-129">Identificatore per l'API Revision ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="6ed24-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="6ed24-130">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6ed24-130">This parameter is required.</span></span>

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

### <span data-ttu-id="6ed24-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ed24-131">-Confirm</span></span>
<span data-ttu-id="6ed24-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ed24-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ed24-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ed24-133">-WhatIf</span></span>
<span data-ttu-id="6ed24-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ed24-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ed24-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6ed24-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ed24-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ed24-136">CommonParameters</span></span>
<span data-ttu-id="6ed24-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ed24-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ed24-138">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6ed24-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ed24-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="6ed24-139">INPUTS</span></span>

### <span data-ttu-id="6ed24-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6ed24-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6ed24-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6ed24-141">System.String</span></span>

### <span data-ttu-id="6ed24-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="6ed24-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="6ed24-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ed24-143">OUTPUTS</span></span>

### <span data-ttu-id="6ed24-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="6ed24-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="6ed24-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="6ed24-145">NOTES</span></span>

## <span data-ttu-id="6ed24-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ed24-146">RELATED LINKS</span></span>

[<span data-ttu-id="6ed24-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="6ed24-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="6ed24-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="6ed24-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)
