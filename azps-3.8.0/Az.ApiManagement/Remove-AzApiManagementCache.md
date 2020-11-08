---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCache.md
ms.openlocfilehash: b43aba64f30c4a1987f2bcd8dec3edb7834f2082
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020186"
---
# <span data-ttu-id="2eaeb-101">Remove-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2eaeb-101">Remove-AzApiManagementCache</span></span>

## <span data-ttu-id="2eaeb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2eaeb-102">SYNOPSIS</span></span>
<span data-ttu-id="2eaeb-103">Rimuove l'entità cache.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-103">Removes the cache entity.</span></span>

## <span data-ttu-id="2eaeb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2eaeb-104">SYNTAX</span></span>

### <span data-ttu-id="2eaeb-105">ContextParameterSetName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2eaeb-105">ContextParameterSetName (Default)</span></span>
```
Remove-AzApiManagementCache -Context <PsApiManagementContext> -CacheId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eaeb-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2eaeb-106">ByInputObjectParameterSet</span></span>
```
Remove-AzApiManagementCache -InputObject <PsApiManagementCache> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eaeb-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2eaeb-107">ByResourceIdParameterSet</span></span>
```
Remove-AzApiManagementCache -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eaeb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2eaeb-108">DESCRIPTION</span></span>
<span data-ttu-id="2eaeb-109">Il cmdlet **Remove-AzApiManagementCache** rimuove l'entità cache.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-109">The cmdlet **Remove-AzApiManagementCache** removes the cache entity.</span></span>

## <span data-ttu-id="2eaeb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2eaeb-110">EXAMPLES</span></span>

### <span data-ttu-id="2eaeb-111">Esempio 1: rimuovere l'entità della cache</span><span class="sxs-lookup"><span data-stu-id="2eaeb-111">Example 1 : Remove the Cache entity</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCache -Context $apimContext -CacheId "centralus"
```

<span data-ttu-id="2eaeb-112">Questo cmdlet consente di rimuovere la cache `centralus` dal servizio di gestione API.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-112">This cmdlet remove the cache `centralus` from Api Management service.</span></span>

## <span data-ttu-id="2eaeb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2eaeb-113">PARAMETERS</span></span>

### <span data-ttu-id="2eaeb-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="2eaeb-114">-CacheId</span></span>
<span data-ttu-id="2eaeb-115">Identificatore della cacheId esistente.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-115">Identifier of existing cacheId.</span></span>
<span data-ttu-id="2eaeb-116">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-116">This parameter is required.</span></span>

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

### <span data-ttu-id="2eaeb-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2eaeb-117">-Context</span></span>
<span data-ttu-id="2eaeb-118">Istanza di PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2eaeb-119">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-119">This parameter is required.</span></span>

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

### <span data-ttu-id="2eaeb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eaeb-120">-DefaultProfile</span></span>
<span data-ttu-id="2eaeb-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eaeb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2eaeb-122">-InputObject</span></span>
<span data-ttu-id="2eaeb-123">Istanza di PsApiManagementCache.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-123">Instance of PsApiManagementCache.</span></span> <span data-ttu-id="2eaeb-124">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-124">This parameter is required.</span></span>

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

### <span data-ttu-id="2eaeb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2eaeb-125">-PassThru</span></span>
<span data-ttu-id="2eaeb-126">Se specificato scriverà true nel caso in cui l'operazione venga eseguita correttamente.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-126">If specified will write true in case operation succeeds.</span></span>
<span data-ttu-id="2eaeb-127">Questo parametro è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-127">This parameter is optional.</span></span>
<span data-ttu-id="2eaeb-128">Il valore predefinito è false.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-128">Default value is false.</span></span>

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

### <span data-ttu-id="2eaeb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2eaeb-129">-ResourceId</span></span>
<span data-ttu-id="2eaeb-130">ResourceId del braccio della cache.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-130">Arm ResourceId of Cache.</span></span> <span data-ttu-id="2eaeb-131">Questo parametro è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-131">This parameter is required.</span></span>

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

### <span data-ttu-id="2eaeb-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2eaeb-132">-Confirm</span></span>
<span data-ttu-id="2eaeb-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eaeb-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eaeb-134">-WhatIf</span></span>
<span data-ttu-id="2eaeb-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eaeb-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eaeb-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eaeb-137">CommonParameters</span></span>
<span data-ttu-id="2eaeb-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eaeb-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eaeb-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2eaeb-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eaeb-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2eaeb-140">INPUTS</span></span>

### <span data-ttu-id="2eaeb-141">Microsoft. Azure. Commands. ApiManagement. ServiceManagement. Models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2eaeb-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2eaeb-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2eaeb-142">System.String</span></span>

### <span data-ttu-id="2eaeb-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2eaeb-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2eaeb-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2eaeb-144">OUTPUTS</span></span>

### <span data-ttu-id="2eaeb-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2eaeb-145">System.Boolean</span></span>

## <span data-ttu-id="2eaeb-146">Note</span><span class="sxs-lookup"><span data-stu-id="2eaeb-146">NOTES</span></span>

## <span data-ttu-id="2eaeb-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2eaeb-147">RELATED LINKS</span></span>

[<span data-ttu-id="2eaeb-148">New-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2eaeb-148">New-AzApiManagementCache</span></span>](./New-AzApiManagementCache)

[<span data-ttu-id="2eaeb-149">Set-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2eaeb-149">Set-AzApiManagementCache</span></span>](./Set-AzApiManagementCache.md)

[<span data-ttu-id="2eaeb-150">Get-AzApiManagementCache</span><span class="sxs-lookup"><span data-stu-id="2eaeb-150">Get-AzApiManagementCache</span></span>](./Get-AzApiManagementCache.md)