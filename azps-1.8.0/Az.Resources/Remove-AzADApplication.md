---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADApplication.md
ms.openlocfilehash: eed437a235072972778925c0b94f2d22466399b3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677320"
---
# <span data-ttu-id="59452-101">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="59452-101">Remove-AzADApplication</span></span>

## <span data-ttu-id="59452-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="59452-102">SYNOPSIS</span></span>
<span data-ttu-id="59452-103">Elimina l'applicazione Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="59452-103">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="59452-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59452-104">SYNTAX</span></span>

### <span data-ttu-id="59452-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59452-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzADApplication -ObjectId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59452-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59452-106">ApplicationIdParameterSet</span></span>
```
Remove-AzADApplication -ApplicationId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59452-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="59452-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzADApplication -DisplayName <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59452-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59452-108">InputObjectParameterSet</span></span>
```
Remove-AzADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59452-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="59452-109">DESCRIPTION</span></span>
<span data-ttu-id="59452-110">Elimina l'applicazione Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="59452-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="59452-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59452-111">EXAMPLES</span></span>

### <span data-ttu-id="59452-112">Esempio 1-rimuovere l'applicazione per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="59452-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="59452-113">Rimuove l'applicazione con l'ID oggetto "b4cd1619-80B3-4cfb-9f8f-9f2333425738" dal tenant.</span><span class="sxs-lookup"><span data-stu-id="59452-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="59452-114">Esempio 2-Rimuovere l'applicazione dall'ID applicazione</span><span class="sxs-lookup"><span data-stu-id="59452-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="59452-115">Rimuove l'applicazione con l'ID applicazione ' f9c5ea4f-28f0-401A-A491-491a037fa346' dal tenant.</span><span class="sxs-lookup"><span data-stu-id="59452-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="59452-116">Esempio 3-rimuovere l'applicazione tramite pipe</span><span class="sxs-lookup"><span data-stu-id="59452-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzADApplication
```

<span data-ttu-id="59452-117">Ottiene l'applicazione con l'ID oggetto "b4cd1619-80B3-4cfb-9f8f-9f2333425738" e le pipe al cmdlet Remove-AzADApplication per rimuovere l'applicazione dal tenant.</span><span class="sxs-lookup"><span data-stu-id="59452-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="59452-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="59452-118">PARAMETERS</span></span>

### <span data-ttu-id="59452-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="59452-119">-ApplicationId</span></span>
<span data-ttu-id="59452-120">ID applicazione dell'applicazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="59452-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="59452-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59452-121">-DefaultProfile</span></span>
<span data-ttu-id="59452-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="59452-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59452-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="59452-123">-DisplayName</span></span>
<span data-ttu-id="59452-124">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="59452-124">The display name of the application.</span></span>

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

### <span data-ttu-id="59452-125">-Force</span><span class="sxs-lookup"><span data-stu-id="59452-125">-Force</span></span>
<span data-ttu-id="59452-126">Passare a eliminare un'applicazione senza conferma.</span><span class="sxs-lookup"><span data-stu-id="59452-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="59452-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59452-127">-InputObject</span></span>
<span data-ttu-id="59452-128">Oggetto che rappresenta l'applicazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="59452-128">The object representing the application to remove.</span></span>

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

### <span data-ttu-id="59452-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="59452-129">-ObjectId</span></span>
<span data-ttu-id="59452-130">ID oggetto dell'applicazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="59452-130">The object id of the application to delete.</span></span>

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

### <span data-ttu-id="59452-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59452-131">-PassThru</span></span>
<span data-ttu-id="59452-132">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="59452-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="59452-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="59452-133">-Confirm</span></span>
<span data-ttu-id="59452-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59452-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59452-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59452-135">-WhatIf</span></span>
<span data-ttu-id="59452-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59452-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59452-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="59452-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59452-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59452-138">CommonParameters</span></span>
<span data-ttu-id="59452-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59452-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59452-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59452-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59452-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="59452-141">INPUTS</span></span>

### <span data-ttu-id="59452-142">System. String</span><span class="sxs-lookup"><span data-stu-id="59452-142">System.String</span></span>

### <span data-ttu-id="59452-143">System. Guid</span><span class="sxs-lookup"><span data-stu-id="59452-143">System.Guid</span></span>

### <span data-ttu-id="59452-144">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="59452-144">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="59452-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59452-145">OUTPUTS</span></span>

### <span data-ttu-id="59452-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="59452-146">System.Boolean</span></span>

## <span data-ttu-id="59452-147">Note</span><span class="sxs-lookup"><span data-stu-id="59452-147">NOTES</span></span>
<span data-ttu-id="59452-148">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="59452-148">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="59452-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59452-149">RELATED LINKS</span></span>

[<span data-ttu-id="59452-150">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="59452-150">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="59452-151">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="59452-151">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="59452-152">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="59452-152">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="59452-153">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="59452-153">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)
