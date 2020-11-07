---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: f816488e6334c0e9c410bb1c24f46501a1fefe85
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673605"
---
# <span data-ttu-id="01caf-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="01caf-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="01caf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="01caf-102">SYNOPSIS</span></span>
<span data-ttu-id="01caf-103">Crea una versione API di una revisione API</span><span class="sxs-lookup"><span data-stu-id="01caf-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="01caf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01caf-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="01caf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="01caf-105">DESCRIPTION</span></span>

<span data-ttu-id="01caf-106">Il cmdlet **New-AzApiManagementApiRelease** crea una versione API per una revisione API nel contesto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="01caf-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span>

## <span data-ttu-id="01caf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01caf-107">EXAMPLES</span></span>

### <span data-ttu-id="01caf-108">Esempio 1: creare una versione API per una revisione API</span><span class="sxs-lookup"><span data-stu-id="01caf-108">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="01caf-109">Questo comando crea una versione API di revisione `2` di `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="01caf-109">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="01caf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="01caf-110">PARAMETERS</span></span>

### <span data-ttu-id="01caf-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="01caf-111">-ApiId</span></span>
<span data-ttu-id="01caf-112">Identificatore per la nuova API.</span><span class="sxs-lookup"><span data-stu-id="01caf-112">Identifier for new API.</span></span>

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

### <span data-ttu-id="01caf-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="01caf-113">-ApiRevision</span></span>
<span data-ttu-id="01caf-114">Identificatore per la revisione API.</span><span class="sxs-lookup"><span data-stu-id="01caf-114">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="01caf-115">-Contesto</span><span class="sxs-lookup"><span data-stu-id="01caf-115">-Context</span></span>
<span data-ttu-id="01caf-116">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="01caf-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="01caf-117">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="01caf-117">This parameter is required.</span></span>

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

### <span data-ttu-id="01caf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01caf-118">-DefaultProfile</span></span>
<span data-ttu-id="01caf-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01caf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01caf-120">-Nota</span><span class="sxs-lookup"><span data-stu-id="01caf-120">-Note</span></span>
<span data-ttu-id="01caf-121">Note sulla versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="01caf-121">Api Release Notes.</span></span> <span data-ttu-id="01caf-122">Questo parametro è facoltativo</span><span class="sxs-lookup"><span data-stu-id="01caf-122">This parameter is optional</span></span>

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

### <span data-ttu-id="01caf-123">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="01caf-123">-ReleaseId</span></span>
<span data-ttu-id="01caf-124">Identificatore per la versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="01caf-124">Identifier for the Api Release.</span></span>
<span data-ttu-id="01caf-125">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="01caf-125">This parameter is optional.</span></span>
<span data-ttu-id="01caf-126">Se l'identificatore non specificato verrà generato.</span><span class="sxs-lookup"><span data-stu-id="01caf-126">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="01caf-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="01caf-127">-Confirm</span></span>
<span data-ttu-id="01caf-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01caf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01caf-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01caf-129">-WhatIf</span></span>
<span data-ttu-id="01caf-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01caf-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="01caf-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01caf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01caf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01caf-132">CommonParameters</span></span>
<span data-ttu-id="01caf-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01caf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01caf-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01caf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01caf-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="01caf-135">INPUTS</span></span>

### <span data-ttu-id="01caf-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="01caf-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="01caf-137">System. String</span><span class="sxs-lookup"><span data-stu-id="01caf-137">System.String</span></span>

## <span data-ttu-id="01caf-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01caf-138">OUTPUTS</span></span>

### <span data-ttu-id="01caf-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="01caf-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="01caf-140">Note</span><span class="sxs-lookup"><span data-stu-id="01caf-140">NOTES</span></span>

## <span data-ttu-id="01caf-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01caf-141">RELATED LINKS</span></span>

[<span data-ttu-id="01caf-142">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="01caf-142">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="01caf-143">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="01caf-143">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="01caf-144">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="01caf-144">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)