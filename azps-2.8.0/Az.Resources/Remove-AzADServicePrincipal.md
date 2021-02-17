---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 0C8C07CA-6720-452F-A952-48C76EBF3BBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADServicePrincipal.md
ms.openlocfilehash: 2658e5ff70603cb9bbe3aa3a7ccd47713249c726
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413490"
---
# <span data-ttu-id="03504-101">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="03504-101">Remove-AzADServicePrincipal</span></span>

## <span data-ttu-id="03504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03504-102">SYNOPSIS</span></span>
<span data-ttu-id="03504-103">Elimina l'entità servizio Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="03504-103">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="03504-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03504-104">SYNTAX</span></span>

### <span data-ttu-id="03504-105">ObjectIdParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03504-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADServicePrincipal -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03504-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="03504-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03504-107">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="03504-107">SPNParameterSet</span></span>
```
Remove-AzADServicePrincipal -ServicePrincipalName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03504-108">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="03504-108">DisplayNameParameterSet</span></span>
```
Remove-AzADServicePrincipal -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03504-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03504-109">InputObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="03504-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="03504-110">ApplicationObjectParameterSet</span></span>
```
Remove-AzADServicePrincipal -ApplicationObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03504-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03504-111">DESCRIPTION</span></span>
<span data-ttu-id="03504-112">Elimina l'entità servizio Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="03504-112">Deletes the azure active directory service principal.</span></span>

## <span data-ttu-id="03504-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03504-113">EXAMPLES</span></span>

### <span data-ttu-id="03504-114">Esempio 1 - Rimuovere un'entità servizio in base all'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="03504-114">Example 1 - Remove a service principal by object id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45
```

<span data-ttu-id="03504-115">Rimuove l'entità servizio con ID oggetto '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span><span class="sxs-lookup"><span data-stu-id="03504-115">Removes the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45'.</span></span>

### <span data-ttu-id="03504-116">Esempio 2 - Rimuovere un'entità servizio in base all'ID applicazione</span><span class="sxs-lookup"><span data-stu-id="03504-116">Example 2 - Remove a service principal by application id</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76
```

<span data-ttu-id="03504-117">Rimuove l'entità servizio con ID applicazione '9263469e-d328-4321-8646-3e3e75d20e76'.</span><span class="sxs-lookup"><span data-stu-id="03504-117">Removes the service principal with application id '9263469e-d328-4321-8646-3e3e75d20e76'.</span></span>

### <span data-ttu-id="03504-118">Esempio 3 - Rimuovere un'entità servizio per SPN</span><span class="sxs-lookup"><span data-stu-id="03504-118">Example 3 - Remove a service principal by SPN</span></span>

```
PS C:\> Remove-AzADServicePrincipal -ServicePrincipalName MyServicePrincipal
```

<span data-ttu-id="03504-119">Rimuovere l'entità servizio con il nome dell'entità servizio "MyServicePrincipal"</span><span class="sxs-lookup"><span data-stu-id="03504-119">Remove the service principal with service principal name "MyServicePrincipal"</span></span>

### <span data-ttu-id="03504-120">Esempio 4 - Rimuovere un'entità servizio tramite piping</span><span class="sxs-lookup"><span data-stu-id="03504-120">Example 4 - Remove a service principal by piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 61b5d8ea-fdc6-40a2-8d5b-ad447c678d45 | Remove-AzADServicePrincipal
```

<span data-ttu-id="03504-121">Ottiene l'entità servizio con ID oggetto '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' e pipe che al cmdlet di Remove-AzADServicePrincipal per rimuovere tale entità servizio.</span><span class="sxs-lookup"><span data-stu-id="03504-121">Gets the service principal with object id '61b5d8ea-fdc6-40a2-8d5b-ad447c678d45' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove that service principal.</span></span>

### <span data-ttu-id="03504-122">Esempio 5 - Rimuovere un'entità servizio tramite piping di un'applicazione</span><span class="sxs-lookup"><span data-stu-id="03504-122">Example 5 - Remove a service principal by piping an application</span></span>

```
PS C:\> Get-AzApplication -ApplicationId 9263469e-d328-4321-8646-3e3e75d20e76 | Remove-AzADServicePrincipal
```

<span data-ttu-id="03504-123">Ottiene l'applicazione con ID applicazione '9263469e-d328-4321-8646-3e3e75d20e76' e pipe che al cmdlet di Remove-AzADServicePrincipal per rimuovere l'entità servizio associata all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="03504-123">Gets the application with application id '9263469e-d328-4321-8646-3e3e75d20e76' and pipes that to the Remove-AzADServicePrincipal cmdlet to remove the service principal associated with that application.</span></span>

## <span data-ttu-id="03504-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03504-124">PARAMETERS</span></span>

### <span data-ttu-id="03504-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="03504-125">-ApplicationId</span></span>
<span data-ttu-id="03504-126">ID applicazione dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="03504-126">The service principal application id.</span></span>

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

### <span data-ttu-id="03504-127">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="03504-127">-ApplicationObject</span></span>
<span data-ttu-id="03504-128">Oggetto applicazione la cui entità servizio è in fase di rimozione.</span><span class="sxs-lookup"><span data-stu-id="03504-128">The application object whose service principal is being removed.</span></span>

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

### <span data-ttu-id="03504-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03504-129">-DefaultProfile</span></span>
<span data-ttu-id="03504-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="03504-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03504-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="03504-131">-DisplayName</span></span>
<span data-ttu-id="03504-132">Nome visualizzato dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="03504-132">The display name of the service principal.</span></span>

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

### <span data-ttu-id="03504-133">-Force</span><span class="sxs-lookup"><span data-stu-id="03504-133">-Force</span></span>
<span data-ttu-id="03504-134">Passare all'eliminazione dell'entità servizio senza conferma.</span><span class="sxs-lookup"><span data-stu-id="03504-134">Switch to delete service principal without a confirmation.</span></span>

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

### <span data-ttu-id="03504-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03504-135">-InputObject</span></span>
<span data-ttu-id="03504-136">Oggetto entità servizio.</span><span class="sxs-lookup"><span data-stu-id="03504-136">The service principal object.</span></span>

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

### <span data-ttu-id="03504-137">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="03504-137">-ObjectId</span></span>
<span data-ttu-id="03504-138">ID oggetto dell'entità servizio da eliminare.</span><span class="sxs-lookup"><span data-stu-id="03504-138">The object id of the service principal to delete.</span></span>

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

### <span data-ttu-id="03504-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03504-139">-PassThru</span></span>
<span data-ttu-id="03504-140">Se specificato, restituisce l'entità servizio eliminata.</span><span class="sxs-lookup"><span data-stu-id="03504-140">If specified, returns the deleted service principal.</span></span>

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

### <span data-ttu-id="03504-141">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="03504-141">-ServicePrincipalName</span></span>
<span data-ttu-id="03504-142">Nome dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="03504-142">The service principal name.</span></span>

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

### <span data-ttu-id="03504-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="03504-143">-Confirm</span></span>
<span data-ttu-id="03504-144">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03504-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03504-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03504-145">-WhatIf</span></span>
<span data-ttu-id="03504-146">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03504-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="03504-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="03504-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03504-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03504-148">CommonParameters</span></span>
<span data-ttu-id="03504-149">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03504-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03504-150">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03504-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03504-151">INPUT</span><span class="sxs-lookup"><span data-stu-id="03504-151">INPUTS</span></span>

### <span data-ttu-id="03504-152">System.String</span><span class="sxs-lookup"><span data-stu-id="03504-152">System.String</span></span>

### <span data-ttu-id="03504-153">System.Guid</span><span class="sxs-lookup"><span data-stu-id="03504-153">System.Guid</span></span>

### <span data-ttu-id="03504-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="03504-154">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="03504-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="03504-155">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="03504-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03504-156">OUTPUTS</span></span>

### <span data-ttu-id="03504-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="03504-157">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="03504-158">NOTE</span><span class="sxs-lookup"><span data-stu-id="03504-158">NOTES</span></span>
<span data-ttu-id="03504-159">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione</span><span class="sxs-lookup"><span data-stu-id="03504-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="03504-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03504-160">RELATED LINKS</span></span>

[<span data-ttu-id="03504-161">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="03504-161">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="03504-162">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="03504-162">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)


[<span data-ttu-id="03504-163">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="03504-163">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="03504-164">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="03504-164">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
