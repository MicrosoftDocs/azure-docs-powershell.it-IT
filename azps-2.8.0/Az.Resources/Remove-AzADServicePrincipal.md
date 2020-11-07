---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 0fa6dde8584eb003bd479e9a73ec96176282d83c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93856361"
---
# <span data-ttu-id="54296-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="54296-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="54296-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54296-102">SYNOPSIS</span></span>
<span data-ttu-id="54296-103">Elimina l'entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="54296-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="54296-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54296-104">SYNTAX</span></span>

### <span data-ttu-id="54296-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="54296-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54296-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="54296-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54296-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="54296-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54296-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="54296-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54296-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54296-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54296-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="54296-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54296-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54296-111">DESCRIPTION</span></span>
<span data-ttu-id="54296-112">Elimina l'entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="54296-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="54296-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54296-113">EXAMPLES</span></span>

### <span data-ttu-id="54296-114">Esempio 1-rimuovere un'entità servizio dall'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="54296-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="54296-115">Rimuove l'entità servizio con l'ID oggetto "61b5d8ea-FdC6-40A2-8D5B-ad447c678d45".</span><span class="sxs-lookup"><span data-stu-id="54296-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="54296-116">Esempio 2-rimuovere un'entità servizio dall'ID applicazione</span><span class="sxs-lookup"><span data-stu-id="54296-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="54296-117">Rimuove l'entità servizio con l'ID applicazione "9263469e-D328-4321-8646-3e3e75d20e76".</span><span class="sxs-lookup"><span data-stu-id="54296-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="54296-118">Esempio 3-rimuovere un'entità servizio per SPN</span><span class="sxs-lookup"><span data-stu-id="54296-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="54296-119">Rimuovere l'entità servizio con il nome dell'entità servizio "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="54296-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="54296-120">Esempio 4-rimuovere un'entità servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="54296-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="54296-121">Ottiene l'entità servizio con l'ID oggetto "61b5d8ea-FdC6-40A2-8D5B-ad447c678d45" e le pipe al cmdlet Remove-AzADServicePrincipal per rimuovere tale entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="54296-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="54296-122">Esempio 5-rimuovere un'entità servizio eseguendo il piping di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="54296-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="54296-123">Ottiene l'applicazione con l'ID applicazione ' 9263469e-D328-4321-8646-3e3e75d20e76' e Pipes che al cmdlet Remove-AzADServicePrincipal per rimuovere l'entità servizio associata a tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="54296-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="54296-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54296-124">PARAMETERS</span></span>

### <span data-ttu-id="54296-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="54296-125">-ApplicationId</span></span>
<span data-ttu-id="54296-126">ID applicazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="54296-126">The service principal application id.</span></span>

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

### <span data-ttu-id="54296-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="54296-127">-ApplicationObject</span></span>
<span data-ttu-id="54296-128">Oggetto Application di cui viene rimosso l'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="54296-128">The application object whose service principal is being removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54296-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54296-129">-DefaultProfile</span></span>
<span data-ttu-id="54296-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="54296-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54296-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="54296-131">-DisplayName</span></span>
<span data-ttu-id="54296-132">Nome visualizzato dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="54296-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="54296-133">-Force</span><span class="sxs-lookup"><span data-stu-id="54296-133">-Force</span></span>
<span data-ttu-id="54296-134">Passare a Elimina entità servizio senza conferma.</span><span class="sxs-lookup"><span data-stu-id="54296-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="54296-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54296-135">-InputObject</span></span>
<span data-ttu-id="54296-136">Oggetto Principal del servizio.</span><span class="sxs-lookup"><span data-stu-id="54296-136">The service principal object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54296-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="54296-137">-ObjectId</span></span>
<span data-ttu-id="54296-138">ID oggetto dell'entità servizio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="54296-138">The object id of the service principal to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: PrincipalId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54296-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="54296-139">-PassThru</span></span>
<span data-ttu-id="54296-140">Se specificato, restituisce l'entità di servizio eliminata.</span><span class="sxs-lookup"><span data-stu-id="54296-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="54296-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="54296-141">-ServicePrincipalName</span></span>
<span data-ttu-id="54296-142">Nome dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="54296-142">The service principal name.</span></span>

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

### <span data-ttu-id="54296-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="54296-143">-Confirm</span></span>
<span data-ttu-id="54296-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54296-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54296-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54296-145">-WhatIf</span></span>
<span data-ttu-id="54296-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54296-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54296-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54296-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54296-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54296-148">CommonParameters</span></span>
<span data-ttu-id="54296-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54296-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54296-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54296-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54296-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54296-151">INPUTS</span></span>

### <span data-ttu-id="54296-152">System. String</span><span class="sxs-lookup"><span data-stu-id="54296-152">System.String</span></span>

### <span data-ttu-id="54296-153">System. Guid</span><span class="sxs-lookup"><span data-stu-id="54296-153">System.Guid</span></span>

### <span data-ttu-id="54296-154">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="54296-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="54296-155">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="54296-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="54296-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54296-156">OUTPUTS</span></span>

### <span data-ttu-id="54296-157">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="54296-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="54296-158">Note</span><span class="sxs-lookup"><span data-stu-id="54296-158">NOTES</span></span>
<span data-ttu-id="54296-159">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="54296-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="54296-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54296-160">RELATED LINKS</span></span>

[<span data-ttu-id="54296-161">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="54296-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="54296-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="54296-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="54296-163">Set-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="54296-163">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="54296-164">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="54296-164">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="54296-165">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="54296-165">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
