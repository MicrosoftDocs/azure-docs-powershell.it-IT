---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 317d6dd822b1ef465abf4e6315fa39a480248c42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985444"
---
# <span data-ttu-id="79739-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="79739-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="79739-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79739-102">SYNOPSIS</span></span>
<span data-ttu-id="79739-103">Crea un rilascio API di una revisione dell'API</span><span class="sxs-lookup"><span data-stu-id="79739-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="79739-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79739-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79739-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79739-105">DESCRIPTION</span></span>

<span data-ttu-id="79739-106">Il cmdlet **New-AzApiManagementApiRelease** crea una versione API per una revisione dell'API nel contesto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="79739-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="79739-107">Viene usata una versione per apportare la revisione api come revisione corrente.</span><span class="sxs-lookup"><span data-stu-id="79739-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="79739-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79739-108">EXAMPLES</span></span>

### <span data-ttu-id="79739-109">Esempio 1: Creare una versione dell'API per una revisione dell'API</span><span class="sxs-lookup"><span data-stu-id="79739-109">Example 1: Create an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementApiRelease -Context $context  -ApiId 5adf6fbf0faadf3ad8558065 -ApiRevision 6 -Note "Releasing version 6"


ReleaseId         : 7e4d3fbb43c146c4bf406499ef9411f4
ApiId             : 5adf6fbf0faadf3ad8558065
CreatedDateTime   : 5/17/2018 1:16:29 AM
UpdatedDateTime   : 5/17/2018 1:16:29 AM
Notes             : Releasing version 6
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Mi
                    crosoft.ApiManagement/service/contoso/apis/5adf6fbf0faadf3ad8558065/releases/7e4d3fbb43c146c4bf40649
                    9ef9411f4
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="79739-110">Questo comando crea una versione API della `2` revisione del `echo-api` file .</span><span class="sxs-lookup"><span data-stu-id="79739-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="79739-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79739-111">PARAMETERS</span></span>

### <span data-ttu-id="79739-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="79739-112">-ApiId</span></span>
<span data-ttu-id="79739-113">Identificatore della nuova API.</span><span class="sxs-lookup"><span data-stu-id="79739-113">Identifier for new API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79739-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="79739-114">-ApiRevision</span></span>
<span data-ttu-id="79739-115">Identificatore della revisione api.</span><span class="sxs-lookup"><span data-stu-id="79739-115">Identifier for the Api Revision.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79739-116">-Context</span><span class="sxs-lookup"><span data-stu-id="79739-116">-Context</span></span>
<span data-ttu-id="79739-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="79739-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="79739-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="79739-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79739-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79739-119">-DefaultProfile</span></span>
<span data-ttu-id="79739-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79739-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79739-121">-Nota</span><span class="sxs-lookup"><span data-stu-id="79739-121">-Note</span></span>
<span data-ttu-id="79739-122">Note sulla versione dell'Api.</span><span class="sxs-lookup"><span data-stu-id="79739-122">Api Release Notes.</span></span> <span data-ttu-id="79739-123">Questo parametro è facoltativo</span><span class="sxs-lookup"><span data-stu-id="79739-123">This parameter is optional</span></span>

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

### <span data-ttu-id="79739-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="79739-124">-ReleaseId</span></span>
<span data-ttu-id="79739-125">Identificatore per la versione api.</span><span class="sxs-lookup"><span data-stu-id="79739-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="79739-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="79739-126">This parameter is optional.</span></span>
<span data-ttu-id="79739-127">Se l'identificatore non viene specificato, verrà generato.</span><span class="sxs-lookup"><span data-stu-id="79739-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="79739-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79739-128">-Confirm</span></span>
<span data-ttu-id="79739-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79739-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79739-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79739-130">-WhatIf</span></span>
<span data-ttu-id="79739-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79739-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79739-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79739-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79739-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79739-133">CommonParameters</span></span>
<span data-ttu-id="79739-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79739-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79739-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79739-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79739-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="79739-136">INPUTS</span></span>

### <span data-ttu-id="79739-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="79739-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="79739-138">System.String</span><span class="sxs-lookup"><span data-stu-id="79739-138">System.String</span></span>

## <span data-ttu-id="79739-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79739-139">OUTPUTS</span></span>

### <span data-ttu-id="79739-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="79739-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="79739-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="79739-141">NOTES</span></span>

## <span data-ttu-id="79739-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79739-142">RELATED LINKS</span></span>

[<span data-ttu-id="79739-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="79739-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="79739-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="79739-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="79739-145">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="79739-145">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)