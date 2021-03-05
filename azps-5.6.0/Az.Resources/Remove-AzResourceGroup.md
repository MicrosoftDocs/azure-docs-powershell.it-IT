---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: d85a6170505563daf1033df60474fd94011d928f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974381"
---
# <span data-ttu-id="88b3b-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88b3b-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="88b3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="88b3b-103">Rimuove un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="88b3b-103">Removes a resource group.</span></span>

## <span data-ttu-id="88b3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88b3b-104">SYNTAX</span></span>

### <span data-ttu-id="88b3b-105">RemoveByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88b3b-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88b3b-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="88b3b-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88b3b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="88b3b-107">DESCRIPTION</span></span>
<span data-ttu-id="88b3b-108">Il cmdlet **Remove-AzResourceGroup** rimuove un gruppo di risorse di Azure e le relative risorse dalla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="88b3b-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="88b3b-109">Per eliminare una risorsa, ma uscire dal gruppo di risorse, usare il cmdlet Remove-AzResource risorsa.</span><span class="sxs-lookup"><span data-stu-id="88b3b-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="88b3b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88b3b-110">EXAMPLES</span></span>

### <span data-ttu-id="88b3b-111">Esempio 1: Rimuovere un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="88b3b-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="88b3b-112">Questo comando rimuove il gruppo di risorse ContosoRG01 dalla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="88b3b-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="88b3b-113">Il cmdlet chiede conferma e non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="88b3b-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="88b3b-114">Esempio 2: Rimuovere un gruppo di risorse senza conferma</span><span class="sxs-lookup"><span data-stu-id="88b3b-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Force
```

<span data-ttu-id="88b3b-115">Questo comando usa il cmdlet Get-AzResourceGroup per ottenere il gruppo di risorse ContosoRG01 e quindi lo passa a **Remove-AzResourceGroup** usando l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="88b3b-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span> <span data-ttu-id="88b3b-116">Il *parametro Force* elimina la richiesta di conferma.</span><span class="sxs-lookup"><span data-stu-id="88b3b-116">The *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="88b3b-117">Esempio 3: Rimuovere tutti i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="88b3b-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="88b3b-118">Questo comando usa il cmdlet **Get-AzResourceGroup** per ottenere tutti i gruppi di risorse e quindi li passa **a Remove-AzResourceGroup usando** l'operatore della pipeline.</span><span class="sxs-lookup"><span data-stu-id="88b3b-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="88b3b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88b3b-119">PARAMETERS</span></span>

### <span data-ttu-id="88b3b-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="88b3b-120">-ApiVersion</span></span>
<span data-ttu-id="88b3b-121">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="88b3b-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="88b3b-122">È possibile specificare una versione diversa da quella predefinita.</span><span class="sxs-lookup"><span data-stu-id="88b3b-122">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b3b-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88b3b-123">-AsJob</span></span>
<span data-ttu-id="88b3b-124">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="88b3b-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88b3b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b3b-125">-DefaultProfile</span></span>
<span data-ttu-id="88b3b-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="88b3b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88b3b-127">-Force</span><span class="sxs-lookup"><span data-stu-id="88b3b-127">-Force</span></span>
<span data-ttu-id="88b3b-128">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="88b3b-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88b3b-129">-Id</span><span class="sxs-lookup"><span data-stu-id="88b3b-129">-Id</span></span>
<span data-ttu-id="88b3b-130">Specifica l'ID del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="88b3b-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="88b3b-131">Non sono consentiti caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="88b3b-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88b3b-132">-Name</span><span class="sxs-lookup"><span data-stu-id="88b3b-132">-Name</span></span>
<span data-ttu-id="88b3b-133">Specifica i nomi dei gruppi di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="88b3b-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="88b3b-134">Non sono consentiti caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="88b3b-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88b3b-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="88b3b-135">-Pre</span></span>
<span data-ttu-id="88b3b-136">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="88b3b-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="88b3b-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88b3b-137">-Confirm</span></span>
<span data-ttu-id="88b3b-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88b3b-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b3b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88b3b-139">-WhatIf</span></span>
<span data-ttu-id="88b3b-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88b3b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88b3b-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88b3b-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b3b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b3b-142">CommonParameters</span></span>
<span data-ttu-id="88b3b-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b3b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b3b-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="88b3b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b3b-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="88b3b-145">INPUTS</span></span>

### <span data-ttu-id="88b3b-146">System.String</span><span class="sxs-lookup"><span data-stu-id="88b3b-146">System.String</span></span>

## <span data-ttu-id="88b3b-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88b3b-147">OUTPUTS</span></span>

### <span data-ttu-id="88b3b-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="88b3b-148">System.Boolean</span></span>

## <span data-ttu-id="88b3b-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="88b3b-149">NOTES</span></span>

## <span data-ttu-id="88b3b-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88b3b-150">RELATED LINKS</span></span>

[<span data-ttu-id="88b3b-151">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88b3b-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="88b3b-152">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88b3b-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="88b3b-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="88b3b-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


