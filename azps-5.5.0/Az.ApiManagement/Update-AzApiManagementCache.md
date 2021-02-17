---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100210250"
---
# <span data-ttu-id="12e20-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="12e20-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="12e20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e20-102">SYNOPSIS</span></span>
<span data-ttu-id="12e20-103">aggiorna una cache nel servizio di gestione api.</span><span class="sxs-lookup"><span data-stu-id="12e20-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="12e20-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12e20-104">SYNTAX</span></span>

### <span data-ttu-id="12e20-105">ExpandedParameter (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12e20-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12e20-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="12e20-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12e20-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="12e20-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12e20-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="12e20-108">DESCRIPTION</span></span>
<span data-ttu-id="12e20-109">Il cmdlet **Update-AzApiManagementCache** aggiorna una cache nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="12e20-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="12e20-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12e20-110">EXAMPLES</span></span>

### <span data-ttu-id="12e20-111">Esempio 1: aggiorna la descrizione della cache in centralus</span><span class="sxs-lookup"><span data-stu-id="12e20-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
```powershell
PS D:\github\azure-powershell> $context=New-AzApiManagementContext -ResourceGroupName Api-Default-Central-US -ServiceName contoso
PS D:\github\azure-powershell> Update-AzApiManagementCache -Context $context -CacheId centralus -Description "Team new cache" -PassThru


CacheId              : centralus
Description          : Team new cache
ConnectionString     : {{5cc19889e6ed3b0524c3f7d3}}
AzureRedisResourceId :
Id                   : /subscriptions/subid/resourceGroups/Api-Default-Central-US/providers/M
                       icrosoft.ApiManagement/service/contoso/caches/centralus
ResourceGroupName    : Api-Default-Central-US
ServiceName          : contoso
```

<span data-ttu-id="12e20-112">Aggiorna la descrizione della cache negli Stati Uniti centrali.</span><span class="sxs-lookup"><span data-stu-id="12e20-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="12e20-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12e20-113">PARAMETERS</span></span>

### <span data-ttu-id="12e20-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="12e20-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="12e20-115">Arm ResourceId dell'istanza della cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="12e20-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="12e20-116">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="12e20-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="12e20-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="12e20-117">-CacheId</span></span>
<span data-ttu-id="12e20-118">Identificatore della nuova cache.</span><span class="sxs-lookup"><span data-stu-id="12e20-118">Identifier of new cache.</span></span>
<span data-ttu-id="12e20-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="12e20-119">This parameter is required.</span></span>

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

### <span data-ttu-id="12e20-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="12e20-120">-ConnectionString</span></span>
<span data-ttu-id="12e20-121">Ridisposizione stringa di connessione.</span><span class="sxs-lookup"><span data-stu-id="12e20-121">Redis Connection String.</span></span>
<span data-ttu-id="12e20-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="12e20-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="12e20-123">-Context</span><span class="sxs-lookup"><span data-stu-id="12e20-123">-Context</span></span>
<span data-ttu-id="12e20-124">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="12e20-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="12e20-125">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="12e20-125">This parameter is required.</span></span>

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

### <span data-ttu-id="12e20-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e20-126">-DefaultProfile</span></span>
<span data-ttu-id="12e20-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12e20-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e20-128">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="12e20-128">-Description</span></span>
<span data-ttu-id="12e20-129">Descrizione cache.</span><span class="sxs-lookup"><span data-stu-id="12e20-129">Cache Description.</span></span>
<span data-ttu-id="12e20-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="12e20-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="12e20-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12e20-131">-InputObject</span></span>
<span data-ttu-id="12e20-132">Istanza di PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="12e20-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="12e20-133">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="12e20-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12e20-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="12e20-134">-PassThru</span></span>
<span data-ttu-id="12e20-135">Se si specifica, nell'output verrà scritta l'istanza di Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache che rappresenta la cache modificata.</span><span class="sxs-lookup"><span data-stu-id="12e20-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="12e20-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12e20-136">-ResourceId</span></span>
<span data-ttu-id="12e20-137">Arm ResourceId of Cache.</span><span class="sxs-lookup"><span data-stu-id="12e20-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="12e20-138">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="12e20-138">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12e20-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12e20-139">-Confirm</span></span>
<span data-ttu-id="12e20-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12e20-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e20-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12e20-141">-WhatIf</span></span>
<span data-ttu-id="12e20-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12e20-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12e20-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12e20-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e20-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e20-144">CommonParameters</span></span>
<span data-ttu-id="12e20-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e20-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e20-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="12e20-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e20-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="12e20-147">INPUTS</span></span>

### <span data-ttu-id="12e20-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="12e20-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="12e20-149">System.String</span><span class="sxs-lookup"><span data-stu-id="12e20-149">System.String</span></span>

### <span data-ttu-id="12e20-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="12e20-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="12e20-151">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="12e20-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="12e20-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12e20-152">OUTPUTS</span></span>

### <span data-ttu-id="12e20-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="12e20-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="12e20-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="12e20-154">NOTES</span></span>

## <span data-ttu-id="12e20-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12e20-155">RELATED LINKS</span></span>

[<span data-ttu-id="12e20-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="12e20-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="12e20-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="12e20-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="12e20-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="12e20-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
