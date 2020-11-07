---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementApiRelease.md
ms.openlocfilehash: 1141d671db13c3ea44a7ed7bd003574f3c13615c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675876"
---
# <span data-ttu-id="c78ce-101">Update-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c78ce-101">Update-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="c78ce-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c78ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c78ce-103">Aggiorna una specifica versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="c78ce-103">Updates a particular Api Release.</span></span>

## <span data-ttu-id="c78ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c78ce-104">SYNTAX</span></span>

### <span data-ttu-id="c78ce-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c78ce-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c78ce-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c78ce-106">ByInputObject</span></span>
```
Update-AzApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c78ce-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c78ce-107">DESCRIPTION</span></span>
<span data-ttu-id="c78ce-108">Il cmdlet **Update-AzApiManagementApiRelease** modifica una versione dell'API di gestione di Azure API.</span><span class="sxs-lookup"><span data-stu-id="c78ce-108">The **Update-AzApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="c78ce-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c78ce-109">EXAMPLES</span></span>

### <span data-ttu-id="c78ce-110">Esempio 1: aggiorna una versione dell'API per una revisione API</span><span class="sxs-lookup"><span data-stu-id="c78ce-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="c78ce-111">Questo comando Aggiorna la `echo-api-release` versione API dell'API `echo-api` con una nuova nota.</span><span class="sxs-lookup"><span data-stu-id="c78ce-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="c78ce-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c78ce-112">PARAMETERS</span></span>

### <span data-ttu-id="c78ce-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c78ce-113">-ApiId</span></span>
<span data-ttu-id="c78ce-114">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="c78ce-114">Identifier of existing API.</span></span>
<span data-ttu-id="c78ce-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c78ce-115">This parameter is required.</span></span>

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

### <span data-ttu-id="c78ce-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c78ce-116">-Context</span></span>
<span data-ttu-id="c78ce-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c78ce-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c78ce-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c78ce-118">This parameter is required.</span></span>

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

### <span data-ttu-id="c78ce-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c78ce-119">-DefaultProfile</span></span>
<span data-ttu-id="c78ce-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c78ce-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c78ce-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c78ce-121">-InputObject</span></span>
<span data-ttu-id="c78ce-122">Istanza di tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="c78ce-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="c78ce-123">-Nota</span><span class="sxs-lookup"><span data-stu-id="c78ce-123">-Note</span></span>
<span data-ttu-id="c78ce-124">Note sulla versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="c78ce-124">Api Release Notes.</span></span>
<span data-ttu-id="c78ce-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c78ce-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="c78ce-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c78ce-126">-PassThru</span></span>
<span data-ttu-id="c78ce-127">Se specificato, quindi istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease che rappresenta la versione dell'API set.</span><span class="sxs-lookup"><span data-stu-id="c78ce-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="c78ce-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="c78ce-128">-ReleaseId</span></span>
<span data-ttu-id="c78ce-129">Identificatore per il ReleaseId di revisione API.</span><span class="sxs-lookup"><span data-stu-id="c78ce-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="c78ce-130">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="c78ce-130">This parameter is required.</span></span>

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

### <span data-ttu-id="c78ce-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c78ce-131">-Confirm</span></span>
<span data-ttu-id="c78ce-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c78ce-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c78ce-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c78ce-133">-WhatIf</span></span>
<span data-ttu-id="c78ce-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c78ce-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c78ce-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c78ce-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c78ce-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c78ce-136">CommonParameters</span></span>
<span data-ttu-id="c78ce-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c78ce-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c78ce-138">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c78ce-138">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c78ce-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c78ce-139">INPUTS</span></span>

### <span data-ttu-id="c78ce-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c78ce-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c78ce-141">System. String</span><span class="sxs-lookup"><span data-stu-id="c78ce-141">System.String</span></span>

### <span data-ttu-id="c78ce-142">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c78ce-142">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="c78ce-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c78ce-143">OUTPUTS</span></span>

### <span data-ttu-id="c78ce-144">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c78ce-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="c78ce-145">Note</span><span class="sxs-lookup"><span data-stu-id="c78ce-145">NOTES</span></span>

## <span data-ttu-id="c78ce-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c78ce-146">RELATED LINKS</span></span>

[<span data-ttu-id="c78ce-147">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c78ce-147">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="c78ce-148">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="c78ce-148">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)