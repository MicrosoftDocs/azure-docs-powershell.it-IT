---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementCache.md
ms.openlocfilehash: 2ac2eb7cb40cb7df4324aff276137527d4b148a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191700"
---
# <span data-ttu-id="05bba-101">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="05bba-101">Update-AzApiManagementCache</span></span>

## <span data-ttu-id="05bba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05bba-102">SYNOPSIS</span></span>
<span data-ttu-id="05bba-103">Aggiorna una cache nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="05bba-103">updates a cache in Api Management service.</span></span>

## <span data-ttu-id="05bba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05bba-104">SYNTAX</span></span>

### <span data-ttu-id="05bba-105">ExpandedParameter (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="05bba-105">ExpandedParameter (Default)</span></span>
```
Update-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05bba-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="05bba-106">ByInputObject</span></span>
```
Update-AzApiManagementCache -InputObject <PsApiManagementCache> [-ConnectionString <String>]
 [-AzureRedisResourceId <String>] [-Description <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05bba-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="05bba-107">ByResourceId</span></span>
```
Update-AzApiManagementCache -ResourceId <String> [-ConnectionString <String>] [-AzureRedisResourceId <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="05bba-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05bba-108">DESCRIPTION</span></span>
<span data-ttu-id="05bba-109">Il cmdlet **Update-AzApiManagementCache** aggiorna una cache nel servizio ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="05bba-109">The cmdlet **Update-AzApiManagementCache** updates a cache in the ApiManagement service.</span></span>

## <span data-ttu-id="05bba-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05bba-110">EXAMPLES</span></span>

### <span data-ttu-id="05bba-111">Esempio 1: aggiorna la descrizione della cache in centralus</span><span class="sxs-lookup"><span data-stu-id="05bba-111">Example 1 : Updates the Description of the Cache in centralus</span></span>
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

<span data-ttu-id="05bba-112">Aggiorna la descrizione della cache negli Stati Uniti centrali.</span><span class="sxs-lookup"><span data-stu-id="05bba-112">Updates the description of the Cache in Central US.</span></span>

## <span data-ttu-id="05bba-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05bba-113">PARAMETERS</span></span>

### <span data-ttu-id="05bba-114">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="05bba-114">-AzureRedisResourceId</span></span>
<span data-ttu-id="05bba-115">ARM ResourceId dell'istanza della cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="05bba-115">Arm ResourceId of the Azure Redis Cache instance.</span></span>
<span data-ttu-id="05bba-116">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="05bba-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="05bba-117">-CacheId</span><span class="sxs-lookup"><span data-stu-id="05bba-117">-CacheId</span></span>
<span data-ttu-id="05bba-118">Identificatore della nuova cache.</span><span class="sxs-lookup"><span data-stu-id="05bba-118">Identifier of new cache.</span></span>
<span data-ttu-id="05bba-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="05bba-119">This parameter is required.</span></span>

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

### <span data-ttu-id="05bba-120">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="05bba-120">-ConnectionString</span></span>
<span data-ttu-id="05bba-121">Stringa di connessione Redis.</span><span class="sxs-lookup"><span data-stu-id="05bba-121">Redis Connection String.</span></span>
<span data-ttu-id="05bba-122">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="05bba-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="05bba-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="05bba-123">-Context</span></span>
<span data-ttu-id="05bba-124">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="05bba-124">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="05bba-125">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="05bba-125">This parameter is required.</span></span>

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

### <span data-ttu-id="05bba-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05bba-126">-DefaultProfile</span></span>
<span data-ttu-id="05bba-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05bba-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05bba-128">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="05bba-128">-Description</span></span>
<span data-ttu-id="05bba-129">Descrizione della cache.</span><span class="sxs-lookup"><span data-stu-id="05bba-129">Cache Description.</span></span>
<span data-ttu-id="05bba-130">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="05bba-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="05bba-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05bba-131">-InputObject</span></span>
<span data-ttu-id="05bba-132">Istanza di PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="05bba-132">Instance of PsApiManagementCache.</span></span>
<span data-ttu-id="05bba-133">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="05bba-133">This parameter is required.</span></span>

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

### <span data-ttu-id="05bba-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05bba-134">-PassThru</span></span>
<span data-ttu-id="05bba-135">Se specificato, viene scritta in output l'istanza del tipo Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache che rappresenta la cache modificata.</span><span class="sxs-lookup"><span data-stu-id="05bba-135">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache type  representing the modified cache will be written to output.</span></span>

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

### <span data-ttu-id="05bba-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05bba-136">-ResourceId</span></span>
<span data-ttu-id="05bba-137">ResourceId del braccio della cache.</span><span class="sxs-lookup"><span data-stu-id="05bba-137">Arm ResourceId of Cache.</span></span>
<span data-ttu-id="05bba-138">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="05bba-138">This parameter is required.</span></span>

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

### <span data-ttu-id="05bba-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="05bba-139">-Confirm</span></span>
<span data-ttu-id="05bba-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05bba-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05bba-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05bba-141">-WhatIf</span></span>
<span data-ttu-id="05bba-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05bba-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05bba-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05bba-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05bba-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05bba-144">CommonParameters</span></span>
<span data-ttu-id="05bba-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05bba-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05bba-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05bba-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05bba-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05bba-147">INPUTS</span></span>

### <span data-ttu-id="05bba-148">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="05bba-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="05bba-149">System. String</span><span class="sxs-lookup"><span data-stu-id="05bba-149">System.String</span></span>

### <span data-ttu-id="05bba-150">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="05bba-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

### <span data-ttu-id="05bba-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="05bba-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="05bba-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05bba-152">OUTPUTS</span></span>

### <span data-ttu-id="05bba-153">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="05bba-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="05bba-154">Note</span><span class="sxs-lookup"><span data-stu-id="05bba-154">NOTES</span></span>

## <span data-ttu-id="05bba-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05bba-155">RELATED LINKS</span></span>

[<span data-ttu-id="05bba-156">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="05bba-156">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache.md)

[<span data-ttu-id="05bba-157">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="05bba-157">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="05bba-158">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="05bba-158">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)
