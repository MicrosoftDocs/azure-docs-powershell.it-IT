---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapirevision
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiRevision.md
ms.openlocfilehash: cd32f29a0202fa8c38abed43075a8623efe068a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507760"
---
# <span data-ttu-id="6e0c5-101">Remove-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6e0c5-101">Remove-AzureRmApiManagementApiRevision</span></span>

## <span data-ttu-id="6e0c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e0c5-102">SYNOPSIS</span></span>
<span data-ttu-id="6e0c5-103">Rimozione di una particolare revisione dell'API</span><span class="sxs-lookup"><span data-stu-id="6e0c5-103">Removed a particular API Revision</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e0c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e0c5-104">SYNTAX</span></span>

### <span data-ttu-id="6e0c5-105">ByApiId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6e0c5-105">ByApiId (Default)</span></span>
```
Remove-AzureRmApiManagementApiRevision -Context <PsApiManagementContext> -ApiId <String> -ApiRevision <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e0c5-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6e0c5-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiRevision -InputObject <PsApiManagementApi> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e0c5-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e0c5-107">DESCRIPTION</span></span>
<span data-ttu-id="6e0c5-108">Il cmdlet **Remove-AzureRmApiManagementApiRevision** rimuove una particolare revisione API.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-108">The cmdlet **Remove-AzureRmApiManagementApiRevision** removes a particular API revision.</span></span>

## <span data-ttu-id="6e0c5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e0c5-109">EXAMPLES</span></span>

### <span data-ttu-id="6e0c5-110">Esempio 1: rimuovere una revisione API</span><span class="sxs-lookup"><span data-stu-id="6e0c5-110">Example 1: Remove an API Revision</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiRevision -Context $apimContext -ApiId "echo-api" -ApiRevision "2"
```

<span data-ttu-id="6e0c5-111">Questo comando rimuove la `2` revisione dell'API `echo-api` dal servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-111">This command removes the `2` revision of the API `echo-api` from API Management service.</span></span>

## <span data-ttu-id="6e0c5-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e0c5-112">PARAMETERS</span></span>

### <span data-ttu-id="6e0c5-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6e0c5-113">-ApiId</span></span>
<span data-ttu-id="6e0c5-114">Identificatore dell'API.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-114">Identifier of the API.</span></span>
<span data-ttu-id="6e0c5-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-115">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e0c5-116">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6e0c5-116">-ApiRevision</span></span>
<span data-ttu-id="6e0c5-117">Identificatore della revisione API.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-117">Identifier of the API Revision.</span></span> <span data-ttu-id="6e0c5-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-118">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e0c5-119">-Contesto</span><span class="sxs-lookup"><span data-stu-id="6e0c5-119">-Context</span></span>
<span data-ttu-id="6e0c5-120">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-120">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6e0c5-121">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-121">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e0c5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e0c5-122">-DefaultProfile</span></span>
<span data-ttu-id="6e0c5-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e0c5-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e0c5-124">-InputObject</span></span>
<span data-ttu-id="6e0c5-125">Istanza di PsApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-125">Instance of PsApiManagementApiRelease.</span></span> <span data-ttu-id="6e0c5-126">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e0c5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e0c5-127">-PassThru</span></span>
<span data-ttu-id="6e0c5-128">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-128">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="6e0c5-129">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="6e0c5-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6e0c5-130">-Confirm</span></span>
<span data-ttu-id="6e0c5-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e0c5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e0c5-132">-WhatIf</span></span>
<span data-ttu-id="6e0c5-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e0c5-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e0c5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e0c5-135">CommonParameters</span></span>
<span data-ttu-id="6e0c5-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e0c5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e0c5-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e0c5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e0c5-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e0c5-138">INPUTS</span></span>

### <span data-ttu-id="6e0c5-139">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6e0c5-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6e0c5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="6e0c5-140">System.String</span></span>

### <span data-ttu-id="6e0c5-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="6e0c5-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>
<span data-ttu-id="6e0c5-142">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6e0c5-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6e0c5-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e0c5-143">OUTPUTS</span></span>

### <span data-ttu-id="6e0c5-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e0c5-144">System.Boolean</span></span>

## <span data-ttu-id="6e0c5-145">Note</span><span class="sxs-lookup"><span data-stu-id="6e0c5-145">NOTES</span></span>

## <span data-ttu-id="6e0c5-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e0c5-146">RELATED LINKS</span></span>

[<span data-ttu-id="6e0c5-147">Get-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6e0c5-147">Get-AzureRmApiManagementApiRevision</span></span>](./Get-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="6e0c5-148">New-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6e0c5-148">New-AzureRmApiManagementApiRevision</span></span>](./New-AzureRmApiManagementApiRevision.md)

[<span data-ttu-id="6e0c5-149">Set-AzureRmApiManagementApiRevision</span><span class="sxs-lookup"><span data-stu-id="6e0c5-149">Set-AzureRmApiManagementApiRevision</span></span>](./Set-AzureRmApiManagementApiRevision.md)
