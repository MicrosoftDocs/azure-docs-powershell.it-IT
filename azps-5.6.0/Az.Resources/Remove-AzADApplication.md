---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: d4415b2f97cb92c8694c0ca56a3b47d751a065f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986647"
---
# <span data-ttu-id="6998a-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6998a-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="6998a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6998a-102">SYNOPSIS</span></span>
<span data-ttu-id="6998a-103">Elimina l'applicazione Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6998a-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="6998a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6998a-104">SYNTAX</span></span>

### <span data-ttu-id="6998a-105">ObjectIdParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6998a-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6998a-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6998a-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6998a-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6998a-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6998a-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6998a-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6998a-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6998a-109">DESCRIPTION</span></span>
<span data-ttu-id="6998a-110">Elimina l'applicazione Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="6998a-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="6998a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6998a-111">EXAMPLES</span></span>

### <span data-ttu-id="6998a-112">Esempio 1: Rimuovere l'applicazione in base all'ID oggetto</span><span class="sxs-lookup"><span data-stu-id="6998a-112">Example 1: Remove application by object id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="6998a-113">Rimuove l'applicazione con ID oggetto 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' dal tenant.</span><span class="sxs-lookup"><span data-stu-id="6998a-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="6998a-114">Esempio 2: Rimuovere l'applicazione in base all'ID applicazione</span><span class="sxs-lookup"><span data-stu-id="6998a-114">Example 2: Remove application by application id</span></span>

```powershell
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="6998a-115">Rimuove l'applicazione con ID applicazione 'f9c5ea4f-28f0-401a-a491-491a037fa346' dal tenant.</span><span class="sxs-lookup"><span data-stu-id="6998a-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="6998a-116">Esempio 3: Rimuovere un'applicazione tramite piping</span><span class="sxs-lookup"><span data-stu-id="6998a-116">Example 3: Remove application by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="6998a-117">Ottiene l'applicazione con ID oggetto 'b4cd1619-80b3-4cfb-9f8f-9f233425738' e pipe che al cmdlet di Remove-AzADApplication per rimuovere l'applicazione dal tenant.</span><span class="sxs-lookup"><span data-stu-id="6998a-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="6998a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6998a-118">PARAMETERS</span></span>

### <span data-ttu-id="6998a-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6998a-119">-ApplicationId</span></span>
<span data-ttu-id="6998a-120">ID applicazione dell'applicazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6998a-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="6998a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6998a-121">-DefaultProfile</span></span>
<span data-ttu-id="6998a-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6998a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6998a-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6998a-123">-DisplayName</span></span>
<span data-ttu-id="6998a-124">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6998a-124">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6998a-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6998a-125">-Force</span></span>
<span data-ttu-id="6998a-126">Passare all'eliminazione di un'applicazione senza conferma.</span><span class="sxs-lookup"><span data-stu-id="6998a-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="6998a-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6998a-127">-InputObject</span></span>
<span data-ttu-id="6998a-128">Oggetto che rappresenta l'applicazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6998a-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6998a-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="6998a-129">-ObjectId</span></span>
<span data-ttu-id="6998a-130">ID oggetto dell'applicazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="6998a-130">The object id of the application to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6998a-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6998a-131">-PassThru</span></span>
<span data-ttu-id="6998a-132">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6998a-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="6998a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6998a-133">-Confirm</span></span>
<span data-ttu-id="6998a-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6998a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6998a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6998a-135">-WhatIf</span></span>
<span data-ttu-id="6998a-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6998a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6998a-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6998a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6998a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6998a-138">CommonParameters</span></span>
<span data-ttu-id="6998a-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6998a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6998a-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6998a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6998a-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="6998a-141">INPUTS</span></span>

### <span data-ttu-id="6998a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6998a-142">System.String</span></span>

### <span data-ttu-id="6998a-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="6998a-143">System.Guid</span></span>

### <span data-ttu-id="6998a-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="6998a-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="6998a-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6998a-145">OUTPUTS</span></span>

### <span data-ttu-id="6998a-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6998a-146">System.Boolean</span></span>

## <span data-ttu-id="6998a-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="6998a-147">NOTES</span></span>
<span data-ttu-id="6998a-148">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione</span><span class="sxs-lookup"><span data-stu-id="6998a-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="6998a-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6998a-149">RELATED LINKS</span></span>

[<span data-ttu-id="6998a-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6998a-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="6998a-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6998a-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="6998a-152">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="6998a-152">Update-AzADApplication</span></span>](./Update-AzADApplication.md)

[<span data-ttu-id="6998a-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="6998a-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

