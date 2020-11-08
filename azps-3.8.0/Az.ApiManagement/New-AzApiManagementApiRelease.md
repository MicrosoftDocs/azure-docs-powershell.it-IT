---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiRelease.md
ms.openlocfilehash: 9b2b94fbd6a308f9d927483e78e060a273354738
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022956"
---
# <span data-ttu-id="91f27-101">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="91f27-101">New-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="91f27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91f27-102">SYNOPSIS</span></span>
<span data-ttu-id="91f27-103">Crea una versione API di una revisione API</span><span class="sxs-lookup"><span data-stu-id="91f27-103">Creates an API Release of an API Revision</span></span>

## <span data-ttu-id="91f27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91f27-104">SYNTAX</span></span>

```
New-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-ReleaseId <String>] [-Note <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91f27-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91f27-105">DESCRIPTION</span></span>

<span data-ttu-id="91f27-106">Il cmdlet **New-AzApiManagementApiRelease** crea una versione API per una revisione API nel contesto di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="91f27-106">The **New-AzApiManagementApiRelease** cmdlet creates an API Release for an API Revision in API Management context.</span></span> <span data-ttu-id="91f27-107">Viene usata una versione per rendere la revisione dell'API come revisione corrente.</span><span class="sxs-lookup"><span data-stu-id="91f27-107">A Release is used to make the Api Revision as Current Revision.</span></span>

## <span data-ttu-id="91f27-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91f27-108">EXAMPLES</span></span>

### <span data-ttu-id="91f27-109">Esempio 1: creare una versione API per una revisione API</span><span class="sxs-lookup"><span data-stu-id="91f27-109">Example 1: Create an API Release for an API Revision</span></span>
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

<span data-ttu-id="91f27-110">Questo comando crea una versione API di revisione `2` di `echo-api` .</span><span class="sxs-lookup"><span data-stu-id="91f27-110">This command creates an API Release of Revision `2` of the `echo-api`.</span></span>

## <span data-ttu-id="91f27-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91f27-111">PARAMETERS</span></span>

### <span data-ttu-id="91f27-112">-ApiId</span><span class="sxs-lookup"><span data-stu-id="91f27-112">-ApiId</span></span>
<span data-ttu-id="91f27-113">Identificatore per la nuova API.</span><span class="sxs-lookup"><span data-stu-id="91f27-113">Identifier for new API.</span></span>

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

### <span data-ttu-id="91f27-114">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="91f27-114">-ApiRevision</span></span>
<span data-ttu-id="91f27-115">Identificatore per la revisione API.</span><span class="sxs-lookup"><span data-stu-id="91f27-115">Identifier for the Api Revision.</span></span>

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

### <span data-ttu-id="91f27-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="91f27-116">-Context</span></span>
<span data-ttu-id="91f27-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="91f27-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="91f27-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="91f27-118">This parameter is required.</span></span>

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

### <span data-ttu-id="91f27-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91f27-119">-DefaultProfile</span></span>
<span data-ttu-id="91f27-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91f27-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91f27-121">-Nota</span><span class="sxs-lookup"><span data-stu-id="91f27-121">-Note</span></span>
<span data-ttu-id="91f27-122">Note sulla versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="91f27-122">Api Release Notes.</span></span> <span data-ttu-id="91f27-123">Questo parametro è facoltativo</span><span class="sxs-lookup"><span data-stu-id="91f27-123">This parameter is optional</span></span>

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

### <span data-ttu-id="91f27-124">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="91f27-124">-ReleaseId</span></span>
<span data-ttu-id="91f27-125">Identificatore per la versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="91f27-125">Identifier for the Api Release.</span></span>
<span data-ttu-id="91f27-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="91f27-126">This parameter is optional.</span></span>
<span data-ttu-id="91f27-127">Se l'identificatore non specificato verrà generato.</span><span class="sxs-lookup"><span data-stu-id="91f27-127">If not specified identifier will be generated.</span></span>

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

### <span data-ttu-id="91f27-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="91f27-128">-Confirm</span></span>
<span data-ttu-id="91f27-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91f27-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91f27-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91f27-130">-WhatIf</span></span>
<span data-ttu-id="91f27-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91f27-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91f27-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="91f27-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91f27-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91f27-133">CommonParameters</span></span>
<span data-ttu-id="91f27-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91f27-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91f27-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="91f27-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91f27-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91f27-136">INPUTS</span></span>

### <span data-ttu-id="91f27-137">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="91f27-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="91f27-138">System. String</span><span class="sxs-lookup"><span data-stu-id="91f27-138">System.String</span></span>

## <span data-ttu-id="91f27-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91f27-139">OUTPUTS</span></span>

### <span data-ttu-id="91f27-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="91f27-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

## <span data-ttu-id="91f27-141">Note</span><span class="sxs-lookup"><span data-stu-id="91f27-141">NOTES</span></span>

## <span data-ttu-id="91f27-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91f27-142">RELATED LINKS</span></span>

[<span data-ttu-id="91f27-143">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="91f27-143">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="91f27-144">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="91f27-144">Remove-AzApiManagementApiRelease</span></span>](./Remove-AzApiManagementApiRelease.md)

[<span data-ttu-id="91f27-145">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="91f27-145">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)