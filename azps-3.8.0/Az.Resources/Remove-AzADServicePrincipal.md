---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 64742aeab343b4440b54916642ebf371b6d27619
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413371"
---
# <span data-ttu-id="35567-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="35567-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="35567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35567-102">SYNOPSIS</span></span>
<span data-ttu-id="35567-103">Elimina l'entità servizio Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="35567-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="35567-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35567-104">SYNTAX</span></span>

### <span data-ttu-id="35567-105">ObjectIdParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="35567-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35567-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="35567-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35567-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="35567-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35567-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="35567-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35567-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35567-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35567-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="35567-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35567-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="35567-111">DESCRIPTION</span></span>
<span data-ttu-id="35567-112">Elimina l'entità servizio Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="35567-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="35567-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35567-113">EXAMPLES</span></span>

### <span data-ttu-id="35567-114">Esempio 1 - Rimuovere un'entità servizio in base all'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="35567-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="35567-115">Rimuove l'entità servizio con ID oggetto '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span><span class="sxs-lookup"><span data-stu-id="35567-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="35567-116">Esempio 2 - Rimuovere un'entità servizio in base all'ID applicazione</span><span class="sxs-lookup"><span data-stu-id="35567-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="35567-117">Rimuove l'entità servizio con ID applicazione '9263469e-d328-4321-8646-3e3e75d20e76'.</span><span class="sxs-lookup"><span data-stu-id="35567-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="35567-118">Esempio 3 - Rimuovere un'entità servizio per SPN</span><span class="sxs-lookup"><span data-stu-id="35567-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="35567-119">Rimuovere l'entità servizio con il nome dell'entità servizio "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="35567-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="35567-120">Esempio 4 - Rimuovere un'entità servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="35567-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="35567-121">Ottiene l'entità servizio con ID oggetto '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' e pipe che al cmdlet di Remove-AzADServicePrincipal per rimuovere tale entità servizio.</span><span class="sxs-lookup"><span data-stu-id="35567-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="35567-122">Esempio 5 - Rimuovere un'entità servizio tramite piping di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="35567-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="35567-123">Ottiene l'applicazione con ID applicazione '9263469e-d328-4321-8646-3e3e75d20e76' e pipe che al cmdlet di Remove-AzADServicePrincipal per rimuovere l'entità servizio associata all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="35567-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="35567-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35567-124">PARAMETERS</span></span>

### <span data-ttu-id="35567-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="35567-125">-ApplicationId</span></span>
<span data-ttu-id="35567-126">ID applicazione entità servizio.</span><span class="sxs-lookup"><span data-stu-id="35567-126">The service principal application id.</span></span>

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

### <span data-ttu-id="35567-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="35567-127">-ApplicationObject</span></span>
<span data-ttu-id="35567-128">Oggetto applicazione la cui entità servizio è in fase di rimozione.</span><span class="sxs-lookup"><span data-stu-id="35567-128">The application object whose service principal is being removed.</span></span>

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

### <span data-ttu-id="35567-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35567-129">-DefaultProfile</span></span>
<span data-ttu-id="35567-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="35567-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35567-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="35567-131">-DisplayName</span></span>
<span data-ttu-id="35567-132">Nome visualizzato dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="35567-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="35567-133">-Force</span><span class="sxs-lookup"><span data-stu-id="35567-133">-Force</span></span>
<span data-ttu-id="35567-134">Passare all'eliminazione dell'entità servizio senza conferma.</span><span class="sxs-lookup"><span data-stu-id="35567-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="35567-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35567-135">-InputObject</span></span>
<span data-ttu-id="35567-136">Oggetto entità servizio.</span><span class="sxs-lookup"><span data-stu-id="35567-136">The service principal object.</span></span>

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

### <span data-ttu-id="35567-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="35567-137">-ObjectId</span></span>
<span data-ttu-id="35567-138">ID oggetto dell'entità servizio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="35567-138">The object id of the service principal to delete.</span></span>

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

### <span data-ttu-id="35567-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35567-139">-PassThru</span></span>
<span data-ttu-id="35567-140">Se specificato, restituisce l'entità servizio eliminata.</span><span class="sxs-lookup"><span data-stu-id="35567-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="35567-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="35567-141">-ServicePrincipalName</span></span>
<span data-ttu-id="35567-142">Nome dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="35567-142">The service principal name.</span></span>

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

### <span data-ttu-id="35567-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35567-143">-Confirm</span></span>
<span data-ttu-id="35567-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35567-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35567-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35567-145">-WhatIf</span></span>
<span data-ttu-id="35567-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35567-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35567-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35567-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35567-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35567-148">CommonParameters</span></span>
<span data-ttu-id="35567-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35567-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35567-150">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="35567-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35567-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="35567-151">INPUTS</span></span>

### <span data-ttu-id="35567-152">System.String</span><span class="sxs-lookup"><span data-stu-id="35567-152">System.String</span></span>

### <span data-ttu-id="35567-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="35567-153">System.Guid</span></span>

### <span data-ttu-id="35567-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="35567-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="35567-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="35567-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="35567-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35567-156">OUTPUTS</span></span>

### <span data-ttu-id="35567-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="35567-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="35567-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="35567-158">NOTES</span></span>
<span data-ttu-id="35567-159">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione</span><span class="sxs-lookup"><span data-stu-id="35567-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="35567-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35567-160">RELATED LINKS</span></span>

[<span data-ttu-id="35567-161">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="35567-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="35567-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="35567-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)


[<span data-ttu-id="35567-163">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="35567-163">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="35567-164">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="35567-164">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
