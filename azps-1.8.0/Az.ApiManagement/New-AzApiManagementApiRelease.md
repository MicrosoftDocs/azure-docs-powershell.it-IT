---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 5e536d3174a9a71cf4f648172f3d06e6fc5ae79f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401002"
---
# <span data-ttu-id="9373c-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9373c-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="9373c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9373c-102">SYNOPSIS</span></span>
<span data-ttu-id="9373c-103">Crea un rilascio API di una revisione dell'API</span><span class="sxs-lookup"><span data-stu-id="9373c-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="9373c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9373c-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9373c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9373c-105">DESCRIPTION</span></span>

<span data-ttu-id="9373c-106">Il cmdlet **New-AzApiManagementApiRelease** crea una versione API per una revisione dell'API nel contesto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="9373c-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="9373c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9373c-107">EXAMPLES</span></span>

### <span data-ttu-id="9373c-108">Esempio 1: Creare una versione dell'API per una revisione dell'API</span><span class="sxs-lookup"><span data-stu-id="9373c-108">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="9373c-109">Questo comando crea una versione API della `2` revisione di `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="9373c-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="9373c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9373c-110">PARAMETERS</span></span>

### <span data-ttu-id="9373c-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="9373c-111">-ApiId</span></span>
<span data-ttu-id="9373c-112">Identificatore della nuova API.</span><span class="sxs-lookup"><span data-stu-id="9373c-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="9373c-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="9373c-113">-ApiRevision</span></span>
<span data-ttu-id="9373c-114">Identificatore della revisione api.</span><span class="sxs-lookup"><span data-stu-id="9373c-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="9373c-115">-Context</span><span class="sxs-lookup"><span data-stu-id="9373c-115">-Context</span></span>
<span data-ttu-id="9373c-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="9373c-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9373c-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="9373c-117">This parameter is required.</span></span>

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

### <span data-ttu-id="9373c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9373c-118">-DefaultProfile</span></span>
<span data-ttu-id="9373c-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9373c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9373c-120">-Nota</span><span class="sxs-lookup"><span data-stu-id="9373c-120">-Note</span></span>
<span data-ttu-id="9373c-121">Note sulla versione dell'Api.</span><span class="sxs-lookup"><span data-stu-id="9373c-121">Api Release Notes.</span></span> <span data-ttu-id="9373c-122">Questo parametro è facoltativo</span><span class="sxs-lookup"><span data-stu-id="9373c-122">This parameter is optional</span></span>

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

### <span data-ttu-id="9373c-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="9373c-123">-ReleaseId</span></span>
<span data-ttu-id="9373c-124">Identificatore per la versione dell'Api.</span><span class="sxs-lookup"><span data-stu-id="9373c-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="9373c-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="9373c-125">This parameter is optional.</span></span>
<span data-ttu-id="9373c-126">Se l'identificatore non viene specificato, verrà generato.</span><span class="sxs-lookup"><span data-stu-id="9373c-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="9373c-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9373c-127">-Confirm</span></span>
<span data-ttu-id="9373c-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9373c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9373c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9373c-129">-WhatIf</span></span>
<span data-ttu-id="9373c-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9373c-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9373c-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9373c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9373c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9373c-132">CommonParameters</span></span>
<span data-ttu-id="9373c-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9373c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9373c-134">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9373c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9373c-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="9373c-135">INPUTS</span></span>

### <span data-ttu-id="9373c-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9373c-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9373c-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9373c-137">System.String</span></span>

## <span data-ttu-id="9373c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9373c-138">OUTPUTS</span></span>

### <span data-ttu-id="9373c-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9373c-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="9373c-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="9373c-140">NOTES</span></span>

## <span data-ttu-id="9373c-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9373c-141">RELATED LINKS</span></span>

[<span data-ttu-id="9373c-142">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9373c-142">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="9373c-143">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9373c-143">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="9373c-144">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="9373c-144">Update-AzApiManagementApiRelease</span></span>](./Update-AzApiManagementApiRelease.md)