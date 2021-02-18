---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: 26704dd0ff44bf8a9e96dde15ebd52b57fa17ae2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100414561"
---
# <span data-ttu-id="900df-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="900df-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="900df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="900df-102">SYNOPSIS</span></span>
<span data-ttu-id="900df-103">Rimuove l'entità cache.</span><span class="sxs-lookup"><span data-stu-id="900df-103">Removes the cache entity.</span></span>

## <span data-ttu-id="900df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="900df-104">SYNTAX</span></span>

### <span data-ttu-id="900df-105">ContextParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="900df-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="900df-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="900df-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="900df-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="900df-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="900df-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="900df-108">DESCRIPTION</span></span>
<span data-ttu-id="900df-109">Il cmdlet **Remove-AzApiManagementCache rimuove** l'entità cache.</span><span class="sxs-lookup"><span data-stu-id="900df-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="900df-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="900df-110">EXAMPLES</span></span>

### <span data-ttu-id="900df-111">Esempio 1: Rimuovere l'entità Cache</span><span class="sxs-lookup"><span data-stu-id="900df-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="900df-112">Questo cmdlet rimuove la cache `centralus` dal servizio di gestione api.</span><span class="sxs-lookup"><span data-stu-id="900df-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="900df-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="900df-113">PARAMETERS</span></span>

### <span data-ttu-id="900df-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="900df-114">-CacheId</span></span>
<span data-ttu-id="900df-115">Identificatore di cacheId esistente.</span><span class="sxs-lookup"><span data-stu-id="900df-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="900df-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="900df-116">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900df-117">-Context</span><span class="sxs-lookup"><span data-stu-id="900df-117">-Context</span></span>
<span data-ttu-id="900df-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="900df-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="900df-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="900df-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="900df-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="900df-120">-DefaultProfile</span></span>
<span data-ttu-id="900df-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="900df-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="900df-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="900df-122">-InputObject</span></span>
<span data-ttu-id="900df-123">Istanza di PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="900df-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="900df-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="900df-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="900df-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="900df-125">-PassThru</span></span>
<span data-ttu-id="900df-126">Se specificato, write true se l'operazione riesce.</span><span class="sxs-lookup"><span data-stu-id="900df-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="900df-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="900df-127">This parameter is optional.</span></span>
<span data-ttu-id="900df-128">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="900df-128">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900df-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="900df-129">-ResourceId</span></span>
<span data-ttu-id="900df-130">Arm ResourceId of Cache.</span><span class="sxs-lookup"><span data-stu-id="900df-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="900df-131">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="900df-131">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="900df-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="900df-132">-Confirm</span></span>
<span data-ttu-id="900df-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="900df-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="900df-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="900df-134">-WhatIf</span></span>
<span data-ttu-id="900df-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="900df-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="900df-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="900df-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="900df-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="900df-137">CommonParameters</span></span>
<span data-ttu-id="900df-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="900df-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="900df-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="900df-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="900df-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="900df-140">INPUTS</span></span>

### <span data-ttu-id="900df-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="900df-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="900df-142">System.String</span><span class="sxs-lookup"><span data-stu-id="900df-142">System.String</span></span>

### <span data-ttu-id="900df-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="900df-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="900df-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="900df-144">OUTPUTS</span></span>

### <span data-ttu-id="900df-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="900df-145">System.Boolean</span></span>

## <span data-ttu-id="900df-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="900df-146">NOTES</span></span>

## <span data-ttu-id="900df-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="900df-147">RELATED LINKS</span></span>

[<span data-ttu-id="900df-148">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="900df-148">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="900df-149">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="900df-149">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="900df-150">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="900df-150">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
