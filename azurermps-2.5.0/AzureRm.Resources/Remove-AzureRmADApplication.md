---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C791C593-F7D5-4961-97F9-E4909813FFE7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: 73aa80f7d42a2ad29b0e5af0ae5e0e6340691733
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866796"
---
# <span data-ttu-id="e96a0-101">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e96a0-101">Remove-AzureRmADApplication</span></span>

## <span data-ttu-id="e96a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e96a0-102">SYNOPSIS</span></span>
<span data-ttu-id="e96a0-103">Elimina l'applicazione Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e96a0-103">Deletes the azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e96a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e96a0-104">SYNTAX</span></span>

### <span data-ttu-id="e96a0-105">ObjectIdParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e96a0-105">ObjectIdParameterSet (Default)</span></span>
```
Remove-AzureRmADApplication -ObjectId <Guid> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e96a0-106">ApplicationIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e96a0-106">ApplicationIdParameterSet</span></span>
```
Remove-AzureRmADApplication -ApplicationId <Guid> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e96a0-107">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e96a0-107">ApplicationDisplayNameParameterSet</span></span>
```
Remove-AzureRmADApplication -DisplayName <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e96a0-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e96a0-108">InputObjectParameterSet</span></span>
```
Remove-AzureRmADApplication -InputObject <PSADApplication> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e96a0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e96a0-109">DESCRIPTION</span></span>
<span data-ttu-id="e96a0-110">Elimina l'applicazione Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="e96a0-110">Deletes the azure active directory application.</span></span>

## <span data-ttu-id="e96a0-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e96a0-111">EXAMPLES</span></span>

### <span data-ttu-id="e96a0-112">Esempio 1-rimuovere l'applicazione per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="e96a0-112">Example 1 - Remove application by object id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738
```

<span data-ttu-id="e96a0-113">Rimuove l'applicazione con l'ID oggetto "b4cd1619-80B3-4cfb-9f8f-9f2333425738" dal tenant.</span><span class="sxs-lookup"><span data-stu-id="e96a0-113">Removes the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' from the tenant.</span></span>

### <span data-ttu-id="e96a0-114">Esempio 2-Rimuovere l'applicazione dall'ID applicazione</span><span class="sxs-lookup"><span data-stu-id="e96a0-114">Example 2 - Remove application by application id</span></span>

```
PS C:\> Remove-AzureRmADApplication -ApplicationId f9c5ea4f-28f0-401a-a491-491a037fa346
```

<span data-ttu-id="e96a0-115">Rimuove l'applicazione con l'ID applicazione ' f9c5ea4f-28f0-401A-A491-491a037fa346' dal tenant.</span><span class="sxs-lookup"><span data-stu-id="e96a0-115">Removes the application with application id 'f9c5ea4f-28f0-401a-a491-491a037fa346' from the tenant.</span></span>

### <span data-ttu-id="e96a0-116">Esempio 3-rimuovere l'applicazione tramite pipe</span><span class="sxs-lookup"><span data-stu-id="e96a0-116">Example 3 - Remove application by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId b4cd1619-80b3-4cfb-9f8f-9f2333425738 | Remove-AzureRmADApplication
```

<span data-ttu-id="e96a0-117">Ottiene l'applicazione con l'ID oggetto "b4cd1619-80B3-4cfb-9f8f-9f2333425738" e le pipe al cmdlet Remove-AzureRmADApplication per rimuovere l'applicazione dal tenant.</span><span class="sxs-lookup"><span data-stu-id="e96a0-117">Gets the application with object id 'b4cd1619-80b3-4cfb-9f8f-9f2333425738' and pipes that to the Remove-AzureRmADApplication cmdlet to remove the application from the tenant.</span></span>

## <span data-ttu-id="e96a0-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e96a0-118">PARAMETERS</span></span>

### <span data-ttu-id="e96a0-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e96a0-119">-ApplicationId</span></span>
<span data-ttu-id="e96a0-120">ID applicazione dell'applicazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e96a0-120">The application id of the application to remove.</span></span>

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

### <span data-ttu-id="e96a0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e96a0-121">-DefaultProfile</span></span>
<span data-ttu-id="e96a0-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e96a0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e96a0-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e96a0-123">-DisplayName</span></span>
<span data-ttu-id="e96a0-124">Nome visualizzato dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e96a0-124">The display name of the application.</span></span>

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

### <span data-ttu-id="e96a0-125">-Force</span><span class="sxs-lookup"><span data-stu-id="e96a0-125">-Force</span></span>
<span data-ttu-id="e96a0-126">Passare a eliminare un'applicazione senza conferma.</span><span class="sxs-lookup"><span data-stu-id="e96a0-126">Switch to delete an application without a confirmation.</span></span>

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

### <span data-ttu-id="e96a0-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e96a0-127">-InputObject</span></span>
<span data-ttu-id="e96a0-128">Oggetto che rappresenta l'applicazione da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e96a0-128">The object representing the application to remove.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e96a0-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e96a0-129">-ObjectId</span></span>
<span data-ttu-id="e96a0-130">ID oggetto dell'applicazione da eliminare.</span><span class="sxs-lookup"><span data-stu-id="e96a0-130">The object id of the application to delete.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e96a0-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e96a0-131">-PassThru</span></span>
<span data-ttu-id="e96a0-132">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="e96a0-132">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="e96a0-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e96a0-133">-Confirm</span></span>
<span data-ttu-id="e96a0-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e96a0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e96a0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e96a0-135">-WhatIf</span></span>
<span data-ttu-id="e96a0-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e96a0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e96a0-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e96a0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e96a0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e96a0-138">CommonParameters</span></span>
<span data-ttu-id="e96a0-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e96a0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e96a0-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e96a0-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e96a0-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e96a0-141">INPUTS</span></span>

### <span data-ttu-id="e96a0-142">System. Guid</span><span class="sxs-lookup"><span data-stu-id="e96a0-142">System.Guid</span></span>

### <span data-ttu-id="e96a0-143">System. String</span><span class="sxs-lookup"><span data-stu-id="e96a0-143">System.String</span></span>

### <span data-ttu-id="e96a0-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e96a0-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="e96a0-145">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e96a0-145">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="e96a0-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e96a0-146">OUTPUTS</span></span>

### <span data-ttu-id="e96a0-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e96a0-147">System.Boolean</span></span>

## <span data-ttu-id="e96a0-148">Note</span><span class="sxs-lookup"><span data-stu-id="e96a0-148">NOTES</span></span>
<span data-ttu-id="e96a0-149">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="e96a0-149">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="e96a0-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e96a0-150">RELATED LINKS</span></span>

[<span data-ttu-id="e96a0-151">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e96a0-151">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="e96a0-152">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e96a0-152">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)



[<span data-ttu-id="e96a0-153">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e96a0-153">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

