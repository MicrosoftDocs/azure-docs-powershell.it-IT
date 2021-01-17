---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCache.md
ms.openlocfilehash: cfa2024064256b780121aeb489a3e8988b0a688e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478835"
---
# <span data-ttu-id="def97-101">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="def97-101">New-AzApiManagementCache</span></span>

## <span data-ttu-id="def97-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="def97-102">SYNOPSIS</span></span>
<span data-ttu-id="def97-103">Crea una nuova entità cache</span><span class="sxs-lookup"><span data-stu-id="def97-103">Creates a new Cache entity</span></span>

## <span data-ttu-id="def97-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="def97-104">SYNTAX</span></span>

```
New-AzApiManagementCache -Context <PsApiManagementContext> [-CacheId <String>] -ConnectionString <String>
 [-AzureRedisResourceId <String>] [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="def97-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="def97-105">DESCRIPTION</span></span>
<span data-ttu-id="def97-106">Il cmdlet **New-AzApiManagementCache** crea una nuova entità cache nel servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="def97-106">The cmdlet **New-AzApiManagementCache** creates a new cache entity in Api Management service.</span></span>

## <span data-ttu-id="def97-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="def97-107">EXAMPLES</span></span>

### <span data-ttu-id="def97-108">Esempio 1: creare una nuova entità cache</span><span class="sxs-lookup"><span data-stu-id="def97-108">Example 1 : Create a new Cache entity</span></span>
```powershell
PS c:\> New-AzApiManagementCache -Context $context -ConnectionString "teamdemo.redis.cache.windows.net:6380,password=xxxxxx+xxxxx=,ssl=True,abortConnect=False" -Description "Team Cache"

CacheId           : centralus
Description       : Team Cache
ConnectionString  : {{5cc19889e6ed3b0524c3f7d3}}
ResourceId        :
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsof
                    t.ApiManagement/service/contoso/caches/centralus
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="def97-109">I cmdlet creano una nuova entità cache nella posizione master del servizio di gestione delle API.</span><span class="sxs-lookup"><span data-stu-id="def97-109">The cmdlets creates a new cache entity in the master location of the Api Management service.</span></span>

## <span data-ttu-id="def97-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="def97-110">PARAMETERS</span></span>

### <span data-ttu-id="def97-111">-AzureRedisResourceId</span><span class="sxs-lookup"><span data-stu-id="def97-111">-AzureRedisResourceId</span></span>
<span data-ttu-id="def97-112">ARM ResourceId dell'istanza della cache di Azure Redis.</span><span class="sxs-lookup"><span data-stu-id="def97-112">Arm ResourceId of the Azure Redis Cache instance.</span></span> <span data-ttu-id="def97-113">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="def97-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="def97-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="def97-114">-CacheId</span></span>
<span data-ttu-id="def97-115">Identificatore della nuova cache.</span><span class="sxs-lookup"><span data-stu-id="def97-115">Identifier of new cache.</span></span>
<span data-ttu-id="def97-116">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="def97-116">This parameter is optional.</span></span>
<span data-ttu-id="def97-117">Se non viene specificato verrà generato.</span><span class="sxs-lookup"><span data-stu-id="def97-117">If not specified will be generated.</span></span>

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

### <span data-ttu-id="def97-118">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="def97-118">-ConnectionString</span></span>
<span data-ttu-id="def97-119">Stringa di connessione Redis.</span><span class="sxs-lookup"><span data-stu-id="def97-119">Redis Connection String.</span></span>
<span data-ttu-id="def97-120">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="def97-120">This parameter is required.</span></span>

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

### <span data-ttu-id="def97-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="def97-121">-Context</span></span>
<span data-ttu-id="def97-122">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="def97-122">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="def97-123">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="def97-123">This parameter is required.</span></span>

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

### <span data-ttu-id="def97-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="def97-124">-DefaultProfile</span></span>
<span data-ttu-id="def97-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="def97-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="def97-126">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="def97-126">-Description</span></span>
<span data-ttu-id="def97-127">Descrizione della cache.</span><span class="sxs-lookup"><span data-stu-id="def97-127">Cache Description.</span></span>
<span data-ttu-id="def97-128">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="def97-128">This parameter is optional.</span></span>

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

### <span data-ttu-id="def97-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="def97-129">-Confirm</span></span>
<span data-ttu-id="def97-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="def97-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="def97-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="def97-131">-WhatIf</span></span>
<span data-ttu-id="def97-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="def97-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="def97-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="def97-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="def97-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="def97-134">CommonParameters</span></span>
<span data-ttu-id="def97-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="def97-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="def97-136">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="def97-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="def97-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="def97-137">INPUTS</span></span>

### <span data-ttu-id="def97-138">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="def97-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="def97-139">System. String</span><span class="sxs-lookup"><span data-stu-id="def97-139">System.String</span></span>

## <span data-ttu-id="def97-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="def97-140">OUTPUTS</span></span>

### <span data-ttu-id="def97-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="def97-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCache</span></span>

## <span data-ttu-id="def97-142">Note</span><span class="sxs-lookup"><span data-stu-id="def97-142">NOTES</span></span>

## <span data-ttu-id="def97-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="def97-143">RELATED LINKS</span></span>

[<span data-ttu-id="def97-144">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="def97-144">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)

[<span data-ttu-id="def97-145">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="def97-145">Remove-AzApiManagementCache</span></span>](./Remove-AzApiManagementCache.md)

[<span data-ttu-id="def97-146">Update-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="def97-146">Update-AzApiManagementCache</span></span>](./Update-AzApiManagementCache.md)
