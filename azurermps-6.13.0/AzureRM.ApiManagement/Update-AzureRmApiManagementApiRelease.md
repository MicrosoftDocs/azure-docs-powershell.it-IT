---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 5b863c0d0c808c8cb993e4f78f9767d13fb634d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509400"
---
# <span data-ttu-id="a5a39-101">Update-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a5a39-101">Update-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="a5a39-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5a39-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a39-103">Aggiorna una specifica versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="a5a39-103">Updates a particular Api Release.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5a39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5a39-104">SYNTAX</span></span>

### <span data-ttu-id="a5a39-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5a39-105">ExpandedParameter (Default)</span></span>
```
Update-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ReleaseId <String> -ApiId <String>
 [-Note <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5a39-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a5a39-106">ByInputObject</span></span>
```
Update-AzureRmApiManagementApiRelease [-Note <String>] -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5a39-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5a39-107">DESCRIPTION</span></span>
<span data-ttu-id="a5a39-108">Il cmdlet **Update-AzureRmApiManagementApiRelease** modifica una versione dell'API di gestione di Azure API.</span><span class="sxs-lookup"><span data-stu-id="a5a39-108">The **Update-AzureRmApiManagementApiRelease** cmdlet modifies an Azure API Management API Release.</span></span>

## <span data-ttu-id="a5a39-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5a39-109">EXAMPLES</span></span>

### <span data-ttu-id="a5a39-110">Esempio 1: aggiorna una versione dell'API per una revisione API</span><span class="sxs-lookup"><span data-stu-id="a5a39-110">Example 1: Updates an API Release for an API Revision</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Update-AzureRmApiManagementApiRelease -Context $ApiMgmtContext -ApiId "echo-api" -ReleaseId "echo-api-release" -Note "Releasing version 2 of the echo-api to public"
```

<span data-ttu-id="a5a39-111">Questo comando Aggiorna la `echo-api-release` versione API dell'API `echo-api` con una nuova nota.</span><span class="sxs-lookup"><span data-stu-id="a5a39-111">This command updates the `echo-api-release` API Release of the Api `echo-api` with new note.</span></span>

## <span data-ttu-id="a5a39-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5a39-112">PARAMETERS</span></span>

### <span data-ttu-id="a5a39-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a5a39-113">-ApiId</span></span>
<span data-ttu-id="a5a39-114">Identificatore dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="a5a39-114">Identifier of existing API.</span></span>
<span data-ttu-id="a5a39-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5a39-115">This parameter is required.</span></span>

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

### <span data-ttu-id="a5a39-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="a5a39-116">-Context</span></span>
<span data-ttu-id="a5a39-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="a5a39-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="a5a39-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5a39-118">This parameter is required.</span></span>

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

### <span data-ttu-id="a5a39-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a39-119">-DefaultProfile</span></span>
<span data-ttu-id="a5a39-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a39-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a39-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5a39-121">-InputObject</span></span>
<span data-ttu-id="a5a39-122">Istanza di tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="a5a39-122">Instance of type Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease.</span></span>

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

### <span data-ttu-id="a5a39-123">-Nota</span><span class="sxs-lookup"><span data-stu-id="a5a39-123">-Note</span></span>
<span data-ttu-id="a5a39-124">Note sulla versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="a5a39-124">Api Release Notes.</span></span>
<span data-ttu-id="a5a39-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a5a39-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="a5a39-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5a39-126">-PassThru</span></span>
<span data-ttu-id="a5a39-127">Se specificato, quindi istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease che rappresenta la versione dell'API set.</span><span class="sxs-lookup"><span data-stu-id="a5a39-127">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease type representing the set API Release.</span></span>

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

### <span data-ttu-id="a5a39-128">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="a5a39-128">-ReleaseId</span></span>
<span data-ttu-id="a5a39-129">Identificatore per il ReleaseId di revisione API.</span><span class="sxs-lookup"><span data-stu-id="a5a39-129">Identifier for the Api Revision ReleaseId.</span></span>
<span data-ttu-id="a5a39-130">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="a5a39-130">This parameter is required.</span></span>

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

### <span data-ttu-id="a5a39-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5a39-131">-Confirm</span></span>
<span data-ttu-id="a5a39-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5a39-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5a39-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a39-133">-WhatIf</span></span>
<span data-ttu-id="a5a39-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5a39-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5a39-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5a39-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5a39-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a39-136">CommonParameters</span></span>
<span data-ttu-id="a5a39-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a39-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a39-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a39-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a39-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5a39-139">INPUTS</span></span>

### <span data-ttu-id="a5a39-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a5a39-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="a5a39-141">Parameters: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a5a39-141">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="a5a39-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a5a39-142">System.String</span></span>

### <span data-ttu-id="a5a39-143">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a5a39-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="a5a39-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5a39-144">OUTPUTS</span></span>

### <span data-ttu-id="a5a39-145">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a5a39-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="a5a39-146">Note</span><span class="sxs-lookup"><span data-stu-id="a5a39-146">NOTES</span></span>

## <span data-ttu-id="a5a39-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5a39-147">RELATED LINKS</span></span>

[<span data-ttu-id="a5a39-148">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a5a39-148">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="a5a39-149">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="a5a39-149">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)
