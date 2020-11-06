---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRelease.md
ms.openlocfilehash: 71256ab72d8c5c6042aa6c17b184066f96b3a813
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507764"
---
# <span data-ttu-id="e9c16-101">Remove-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e9c16-101">Remove-AzureRmApiManagementApiRelease</span></span>

## <span data-ttu-id="e9c16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9c16-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c16-103">Rimuove una specifica versione dell'API</span><span class="sxs-lookup"><span data-stu-id="e9c16-103">Removes a particular API Release</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9c16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9c16-104">SYNTAX</span></span>

### <span data-ttu-id="e9c16-105">ByApiReleaseId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e9c16-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9c16-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e9c16-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9c16-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9c16-107">DESCRIPTION</span></span>

<span data-ttu-id="e9c16-108">Il cmdlet **Remove-AzureRmApiManagementApiRelease** rimuove una versione API esistente.</span><span class="sxs-lookup"><span data-stu-id="e9c16-108">The **Remove-AzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="e9c16-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9c16-109">EXAMPLES</span></span>

### <span data-ttu-id="e9c16-110">Esempio 1: rimuovere una versione dell'API</span><span class="sxs-lookup"><span data-stu-id="e9c16-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="e9c16-111">Questo comando rimuove il rilascio dell'API con specificato ApiId e ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="e9c16-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="e9c16-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9c16-112">PARAMETERS</span></span>

### <span data-ttu-id="e9c16-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e9c16-113">-ApiId</span></span>
<span data-ttu-id="e9c16-114">Identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="e9c16-114">Identifier of the API.</span></span>
<span data-ttu-id="e9c16-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9c16-115">This parameter is required.</span></span>

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

### <span data-ttu-id="e9c16-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="e9c16-116">-Context</span></span>
<span data-ttu-id="e9c16-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e9c16-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e9c16-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9c16-118">This parameter is required.</span></span>

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

### <span data-ttu-id="e9c16-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c16-119">-DefaultProfile</span></span>
<span data-ttu-id="e9c16-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9c16-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9c16-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9c16-121">-InputObject</span></span>
<span data-ttu-id="e9c16-122">Istanza di PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="e9c16-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="e9c16-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9c16-123">This parameter is required.</span></span>

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

### <span data-ttu-id="e9c16-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e9c16-124">-PassThru</span></span>
<span data-ttu-id="e9c16-125">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="e9c16-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="e9c16-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="e9c16-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="e9c16-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="e9c16-127">-ReleaseId</span></span>
<span data-ttu-id="e9c16-128">Identificatore della versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="e9c16-128">Identifier of the API Release.</span></span>
<span data-ttu-id="e9c16-129">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="e9c16-129">This parameter is required.</span></span>

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

### <span data-ttu-id="e9c16-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e9c16-130">-Confirm</span></span>
<span data-ttu-id="e9c16-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9c16-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9c16-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9c16-132">-WhatIf</span></span>
<span data-ttu-id="e9c16-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9c16-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9c16-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e9c16-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9c16-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c16-135">CommonParameters</span></span>
<span data-ttu-id="e9c16-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9c16-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c16-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9c16-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c16-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9c16-138">INPUTS</span></span>

### <span data-ttu-id="e9c16-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e9c16-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e9c16-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e9c16-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>
<span data-ttu-id="e9c16-141">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e9c16-141">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="e9c16-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e9c16-142">System.String</span></span>

## <span data-ttu-id="e9c16-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9c16-143">OUTPUTS</span></span>

### <span data-ttu-id="e9c16-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9c16-144">System.Boolean</span></span>

## <span data-ttu-id="e9c16-145">Note</span><span class="sxs-lookup"><span data-stu-id="e9c16-145">NOTES</span></span>

## <span data-ttu-id="e9c16-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9c16-146">RELATED LINKS</span></span>

[<span data-ttu-id="e9c16-147">Get-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e9c16-147">Get-AzureRmApiManagementApiRelease</span></span>](./Get-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="e9c16-148">New-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e9c16-148">New-AzureRmApiManagementApiRelease</span></span>](./New-AzureRmApiManagementApiRelease.md)

[<span data-ttu-id="e9c16-149">Set-AzureRmApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="e9c16-149">Set-AzureRmApiManagementApiRelease</span></span>](./Set-AzureRmApiManagementApiRelease.md)
