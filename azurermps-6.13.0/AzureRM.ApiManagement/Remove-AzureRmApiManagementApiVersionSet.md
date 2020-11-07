---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiVersionSet.md
ms.openlocfilehash: 4ff48709b02cdd0270c559ea8be2f4e269dbce2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685456"
---
# <span data-ttu-id="4f6f0-101">Remove-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4f6f0-101">Remove-AzureRmApiManagementApiVersionSet</span></span>

## <span data-ttu-id="4f6f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4f6f0-102">SYNOPSIS</span></span>
<span data-ttu-id="4f6f0-103">Rimuove un set di versioni dell'API specifico</span><span class="sxs-lookup"><span data-stu-id="4f6f0-103">Removes a particular Api Version Set</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f6f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4f6f0-104">SYNTAX</span></span>

### <span data-ttu-id="4f6f0-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4f6f0-105">ExpandedParameter (Default)</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f6f0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4f6f0-106">ByInputObject</span></span>
```
Remove-AzureRmApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f6f0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4f6f0-107">DESCRIPTION</span></span>

<span data-ttu-id="4f6f0-108">Il cmdlet **Remove-AzureRmApiManagementApiVersionSet** rimuove un set di versioni dell'API esistente.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-108">The **Remove-AzureRmApiManagementApiVersionSet** cmdlet removes an existing API Version Set.</span></span>

## <span data-ttu-id="4f6f0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4f6f0-109">EXAMPLES</span></span>

### <span data-ttu-id="4f6f0-110">Esempio 1: rimuovere un set di versioni dell'API</span><span class="sxs-lookup"><span data-stu-id="4f6f0-110">Example 1: Remove an API Version set</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiVersionSet -Context $apimContext -ApiVersionSetId "query-param-set"
```

<span data-ttu-id="4f6f0-111">Questo comando rimuove il set di versioni dell'API con il ApiVersionSetId specificato.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-111">This command removes the API Version Set with the specified ApiVersionSetId.</span></span>

## <span data-ttu-id="4f6f0-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4f6f0-112">PARAMETERS</span></span>

### <span data-ttu-id="4f6f0-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="4f6f0-113">-ApiVersionSetId</span></span>
<span data-ttu-id="4f6f0-114">Identificatore del set di versioni dell'API.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-114">Identifier of the API Version Set.</span></span>
<span data-ttu-id="4f6f0-115">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-115">This parameter is required.</span></span>

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

### <span data-ttu-id="4f6f0-116">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4f6f0-116">-Context</span></span>
<span data-ttu-id="4f6f0-117">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="4f6f0-118">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-118">This parameter is required.</span></span>

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

### <span data-ttu-id="4f6f0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f6f0-119">-DefaultProfile</span></span>
<span data-ttu-id="4f6f0-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f6f0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f6f0-121">-InputObject</span></span>
<span data-ttu-id="4f6f0-122">Istanza di PsApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-122">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="4f6f0-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-123">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f6f0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f6f0-124">-PassThru</span></span>
<span data-ttu-id="4f6f0-125">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-125">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="4f6f0-126">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="4f6f0-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4f6f0-127">-Confirm</span></span>
<span data-ttu-id="4f6f0-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f6f0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f6f0-129">-WhatIf</span></span>
<span data-ttu-id="4f6f0-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f6f0-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f6f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f6f0-132">CommonParameters</span></span>
<span data-ttu-id="4f6f0-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f6f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f6f0-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f6f0-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f6f0-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4f6f0-135">INPUTS</span></span>

### <span data-ttu-id="4f6f0-136">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4f6f0-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>
<span data-ttu-id="4f6f0-137">Parameters: Context (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4f6f0-137">Parameters: Context (ByValue)</span></span>

### <span data-ttu-id="4f6f0-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4f6f0-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>
<span data-ttu-id="4f6f0-139">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4f6f0-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4f6f0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4f6f0-140">System.String</span></span>

## <span data-ttu-id="4f6f0-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4f6f0-141">OUTPUTS</span></span>

### <span data-ttu-id="4f6f0-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f6f0-142">System.Boolean</span></span>

## <span data-ttu-id="4f6f0-143">Note</span><span class="sxs-lookup"><span data-stu-id="4f6f0-143">NOTES</span></span>

## <span data-ttu-id="4f6f0-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4f6f0-144">RELATED LINKS</span></span>

[<span data-ttu-id="4f6f0-145">Get-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4f6f0-145">Get-AzureRmApiManagementApiVersionSet</span></span>](./Get-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="4f6f0-146">New-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4f6f0-146">New-AzureRmApiManagementApiVersionSet</span></span>](./New-AzureRmApiManagementApiVersionSet.md)

[<span data-ttu-id="4f6f0-147">Set-AzureRmApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="4f6f0-147">Set-AzureRmApiManagementApiVersionSet</span></span>](./Set-AzureRmApiManagementApiVersionSet.md)
