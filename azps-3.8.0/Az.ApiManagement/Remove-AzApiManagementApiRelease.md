---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapirelease
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiRelease.md
ms.openlocfilehash: 073f93cdb13e39925ef92dc556fb06a0ac96bcae
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020863"
---
# <span data-ttu-id="b9686-101">Remove-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b9686-101">Remove-AzApiManagementApiRelease</span></span>

## <span data-ttu-id="b9686-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b9686-102">SYNOPSIS</span></span>
<span data-ttu-id="b9686-103">Rimuove una specifica versione dell'API</span><span class="sxs-lookup"><span data-stu-id="b9686-103">Removes a particular API Release</span></span>

## <span data-ttu-id="b9686-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b9686-104">SYNTAX</span></span>

### <span data-ttu-id="b9686-105">ByApiReleaseId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b9686-105">ByApiReleaseId (Default)</span></span>
```
Remove-AzApiManagementApiRelease -Context <PsApiManagementContext> -ApiId <String> -ReleaseId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9686-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b9686-106">ByInputObject</span></span>
```
Remove-AzApiManagementApiRelease -InputObject <PsApiManagementApiRelease> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9686-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b9686-107">DESCRIPTION</span></span>

<span data-ttu-id="b9686-108">Il cmdlet **Remove-AzAzureRmApiManagementApiRelease** rimuove una versione API esistente.</span><span class="sxs-lookup"><span data-stu-id="b9686-108">The **Remove-AzAzureRmApiManagementApiRelease** cmdlet removes an existing API Release.</span></span>

## <span data-ttu-id="b9686-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b9686-109">EXAMPLES</span></span>

### <span data-ttu-id="b9686-110">Esempio 1: rimuovere una versione dell'API</span><span class="sxs-lookup"><span data-stu-id="b9686-110">Example 1: Remove an API Release</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzAzureRmApiManagementApiRelease -Context $apimContext -ApiId "echo-api" -ReleaseId "2"
```

<span data-ttu-id="b9686-111">Questo comando rimuove il rilascio dell'API con specificato ApiId e ReleaseId.</span><span class="sxs-lookup"><span data-stu-id="b9686-111">This command removes the API Release with the specified ApiId and ReleaseId.</span></span>

## <span data-ttu-id="b9686-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b9686-112">PARAMETERS</span></span>

### <span data-ttu-id="b9686-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b9686-113">-ApiId</span></span>
<span data-ttu-id="b9686-114">Identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="b9686-114">Identifier of the API.</span></span>
<span data-ttu-id="b9686-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9686-115">This parameter is required.</span></span>

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

### <span data-ttu-id="b9686-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="b9686-116">-Context</span></span>
<span data-ttu-id="b9686-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b9686-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b9686-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9686-118">This parameter is required.</span></span>

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

### <span data-ttu-id="b9686-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9686-119">-DefaultProfile</span></span>
<span data-ttu-id="b9686-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b9686-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9686-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9686-121">-InputObject</span></span>
<span data-ttu-id="b9686-122">Istanza di PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="b9686-122">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="b9686-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9686-123">This parameter is required.</span></span>

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

### <span data-ttu-id="b9686-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9686-124">-PassThru</span></span>
<span data-ttu-id="b9686-125">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="b9686-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="b9686-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b9686-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="b9686-127">-ReleaseId</span><span class="sxs-lookup"><span data-stu-id="b9686-127">-ReleaseId</span></span>
<span data-ttu-id="b9686-128">Identificatore della versione dell'API.</span><span class="sxs-lookup"><span data-stu-id="b9686-128">Identifier of the API Release.</span></span>
<span data-ttu-id="b9686-129">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="b9686-129">This parameter is required.</span></span>

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

### <span data-ttu-id="b9686-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b9686-130">-Confirm</span></span>
<span data-ttu-id="b9686-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9686-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9686-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9686-132">-WhatIf</span></span>
<span data-ttu-id="b9686-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9686-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9686-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b9686-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9686-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9686-135">CommonParameters</span></span>
<span data-ttu-id="b9686-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9686-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9686-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9686-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9686-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b9686-138">INPUTS</span></span>

### <span data-ttu-id="b9686-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b9686-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b9686-140">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b9686-140">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiRelease</span></span>

### <span data-ttu-id="b9686-141">System. String</span><span class="sxs-lookup"><span data-stu-id="b9686-141">System.String</span></span>

## <span data-ttu-id="b9686-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b9686-142">OUTPUTS</span></span>

### <span data-ttu-id="b9686-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9686-143">System.Boolean</span></span>

## <span data-ttu-id="b9686-144">Note</span><span class="sxs-lookup"><span data-stu-id="b9686-144">NOTES</span></span>

## <span data-ttu-id="b9686-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b9686-145">RELATED LINKS</span></span>

[<span data-ttu-id="b9686-146">Get-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b9686-146">Get-AzApiManagementApiRelease</span></span>](./Get-AzApiManagementApiRelease.md)

[<span data-ttu-id="b9686-147">New-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b9686-147">New-AzApiManagementApiRelease</span></span>](./New-AzApiManagementApiRelease.md)

[<span data-ttu-id="b9686-148">Set-AzApiManagementApiRelease</span><span class="sxs-lookup"><span data-stu-id="b9686-148">Set-AzApiManagementApiRelease</span></span>](./Set-AzApiManagementApiRelease.md)