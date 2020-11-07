---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 462acabd83090a893119d94d93fd767907c5144b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865731"
---
# <span data-ttu-id="0aded-101">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0aded-101">Remove-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="0aded-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0aded-102">SYNOPSIS</span></span>
<span data-ttu-id="0aded-103">Elimina l'entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0aded-103">Deletes the azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0aded-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0aded-104">SYNTAX</span></span>

### <span data-ttu-id="0aded-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0aded-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADServicePrincipal -ObjectId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aded-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aded-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aded-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aded-107">SPNParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aded-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aded-108">DisplayNameParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aded-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aded-109">InputObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0aded-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0aded-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0aded-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0aded-111">DESCRIPTION</span></span>
<span data-ttu-id="0aded-112">Elimina l'entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0aded-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="0aded-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0aded-113">EXAMPLES</span></span>

### <span data-ttu-id="0aded-114">Esempio 1-rimuovere un'entità servizio dall'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="0aded-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="0aded-115">Rimuove l'entità servizio con l'ID oggetto "61b5d8ea-FdC6-40A2-8D5B-ad447c678d45".</span><span class="sxs-lookup"><span data-stu-id="0aded-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="0aded-116">Esempio 2-rimuovere un'entità servizio dall'ID applicazione</span><span class="sxs-lookup"><span data-stu-id="0aded-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="0aded-117">Rimuove l'entità servizio con l'ID applicazione "9263469e-D328-4321-8646-3e3e75d20e76".</span><span class="sxs-lookup"><span data-stu-id="0aded-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="0aded-118">Esempio 3-rimuovere un'entità servizio per SPN</span><span class="sxs-lookup"><span data-stu-id="0aded-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzureRmADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="0aded-119">Rimuovere l'entità servizio con il nome dell'entità servizio "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="0aded-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="0aded-120">Esempio 4-rimuovere un'entità servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="0aded-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="0aded-121">Ottiene l'entità servizio con l'ID oggetto "61b5d8ea-FdC6-40A2-8D5B-ad447c678d45" e le pipe al cmdlet Remove-AzureRmADServicePrincipal per rimuovere tale entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="0aded-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="0aded-122">Esempio 5-rimuovere un'entità servizio eseguendo il piping di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="0aded-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzureRmApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzureRmADServicePrincipal
```

<span data-ttu-id="0aded-123">Ottiene l'applicazione con l'ID applicazione ' 9263469e-D328-4321-8646-3e3e75d20e76' e Pipes che al cmdlet Remove-AzureRmADServicePrincipal per rimuovere l'entità servizio associata a tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="0aded-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzureRmADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="0aded-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0aded-124">PARAMETERS</span></span>

### <span data-ttu-id="0aded-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0aded-125">-ApplicationId</span></span>
<span data-ttu-id="0aded-126">ID applicazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0aded-126">The service principal application id.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aded-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="0aded-127">-ApplicationObject</span></span>
<span data-ttu-id="0aded-128">Oggetto Application di cui viene rimosso l'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="0aded-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0aded-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0aded-129">-DefaultProfile</span></span>
<span data-ttu-id="0aded-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0aded-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0aded-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0aded-131">-DisplayName</span></span>
<span data-ttu-id="0aded-132">Nome visualizzato dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0aded-132">The display name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aded-133">-Force</span><span class="sxs-lookup"><span data-stu-id="0aded-133">-Force</span></span>
<span data-ttu-id="0aded-134">Passare a Elimina entità servizio senza conferma.</span><span class="sxs-lookup"><span data-stu-id="0aded-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="0aded-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0aded-135">-InputObject</span></span>
<span data-ttu-id="0aded-136">Oggetto Principal del servizio.</span><span class="sxs-lookup"><span data-stu-id="0aded-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0aded-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="0aded-137">-ObjectId</span></span>
<span data-ttu-id="0aded-138">ID oggetto dell'entità servizio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="0aded-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aded-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0aded-139">-PassThru</span></span>
<span data-ttu-id="0aded-140">Se specificato, restituisce l'entità di servizio eliminata.</span><span class="sxs-lookup"><span data-stu-id="0aded-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="0aded-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="0aded-141">-ServicePrincipalName</span></span>
<span data-ttu-id="0aded-142">Nome dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0aded-142">The service principal name.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0aded-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0aded-143">-Confirm</span></span>
<span data-ttu-id="0aded-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0aded-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0aded-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0aded-145">-WhatIf</span></span>
<span data-ttu-id="0aded-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0aded-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0aded-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0aded-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0aded-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0aded-148">CommonParameters</span></span>
<span data-ttu-id="0aded-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0aded-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0aded-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0aded-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0aded-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0aded-151">INPUTS</span></span>

### <span data-ttu-id="0aded-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="0aded-152">System.Guid</span></span>

### <span data-ttu-id="0aded-153">System. String</span><span class="sxs-lookup"><span data-stu-id="0aded-153">System.String</span></span>

### <span data-ttu-id="0aded-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0aded-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="0aded-155">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0aded-155">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="0aded-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="0aded-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="0aded-157">Parametri: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0aded-157">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="0aded-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0aded-158">OUTPUTS</span></span>

### <span data-ttu-id="0aded-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0aded-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="0aded-160">Note</span><span class="sxs-lookup"><span data-stu-id="0aded-160">NOTES</span></span>
<span data-ttu-id="0aded-161">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="0aded-161">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0aded-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0aded-162">RELATED LINKS</span></span>

[<span data-ttu-id="0aded-163">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0aded-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="0aded-164">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0aded-164">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



[<span data-ttu-id="0aded-165">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="0aded-165">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="0aded-166">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="0aded-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)
