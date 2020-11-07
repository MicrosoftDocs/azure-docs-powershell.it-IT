---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 31e2151e5c41a4e4c9d053174f9d598cd16680f0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675961"
---
# <span data-ttu-id="0c9ca-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0c9ca-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="0c9ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0c9ca-102">SYNOPSIS</span></span>
<span data-ttu-id="0c9ca-103">Rimuove una specifica versione dell'API</span><span class="sxs-lookup"><span data-stu-id="0c9ca-103">Removes a particular API Release</span></span>

## <span data-ttu-id="0c9ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0c9ca-104">SYNTAX</span></span>

### <span data-ttu-id="0c9ca-105">ByApiReleaseId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0c9ca-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c9ca-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0c9ca-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c9ca-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0c9ca-107">DESCRIPTION</span></span>

<span data-ttu-id="0c9ca-108">Il cmdlet **Remove-AzAzureRmApiManagementApiRelease** rimuove una versione API esistente.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="0c9ca-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0c9ca-109">EXAMPLES</span></span>

### <span data-ttu-id="0c9ca-110">Esempio 1: rimuovere una versione dell'API</span><span class="sxs-lookup"><span data-stu-id="0c9ca-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="0c9ca-111">Questo comando rimuove il rilascio dell'API con specificato ApiId e ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="0c9ca-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0c9ca-112">PARAMETERS</span></span>

### <span data-ttu-id="0c9ca-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0c9ca-113">-ApiId</span></span>
<span data-ttu-id="0c9ca-114">Identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-114">Identifier of the API.</span></span>
<span data-ttu-id="0c9ca-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-115">This parameter is required.</span></span>

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

### <span data-ttu-id="0c9ca-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0c9ca-116">-Context</span></span>
<span data-ttu-id="0c9ca-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0c9ca-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-118">This parameter is required.</span></span>

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

### <span data-ttu-id="0c9ca-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c9ca-119">-DefaultProfile</span></span>
<span data-ttu-id="0c9ca-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c9ca-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c9ca-121">-InputObject</span></span>
<span data-ttu-id="0c9ca-122">Istanza di PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="0c9ca-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-123">This parameter is required.</span></span>

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

### <span data-ttu-id="0c9ca-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c9ca-124">-PassThru</span></span>
<span data-ttu-id="0c9ca-125">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="0c9ca-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="0c9ca-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="0c9ca-127">-ReleaseId</span></span>
<span data-ttu-id="0c9ca-128">Identificatore della versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-128">Identifier of the API Release.</span></span>
<span data-ttu-id="0c9ca-129">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-129">This parameter is required.</span></span>

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

### <span data-ttu-id="0c9ca-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0c9ca-130">-Confirm</span></span>
<span data-ttu-id="0c9ca-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c9ca-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c9ca-132">-WhatIf</span></span>
<span data-ttu-id="0c9ca-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c9ca-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c9ca-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c9ca-135">CommonParameters</span></span>
<span data-ttu-id="0c9ca-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c9ca-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c9ca-137">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0c9ca-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c9ca-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0c9ca-138">INPUTS</span></span>

### <span data-ttu-id="0c9ca-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0c9ca-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0c9ca-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0c9ca-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="0c9ca-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0c9ca-141">System.String</span></span>

## <span data-ttu-id="0c9ca-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0c9ca-142">OUTPUTS</span></span>

### <span data-ttu-id="0c9ca-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0c9ca-143">System.Boolean</span></span>

## <span data-ttu-id="0c9ca-144">Note</span><span class="sxs-lookup"><span data-stu-id="0c9ca-144">NOTES</span></span>

## <span data-ttu-id="0c9ca-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0c9ca-145">RELATED LINKS</span></span>

[<span data-ttu-id="0c9ca-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0c9ca-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="0c9ca-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0c9ca-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="0c9ca-148">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="0c9ca-148">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)