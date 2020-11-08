---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroup.md
ms.openlocfilehash: e53e5311b4553dc3803a4a6d9ac31d6a2569bbc0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188900"
---
# <span data-ttu-id="6e487-101">Remove-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e487-101">Remove-AzResourceGroup</span></span>

## <span data-ttu-id="6e487-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e487-102">SYNOPSIS</span></span>
<span data-ttu-id="6e487-103">Rimuove un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6e487-103">Removes a resource group.</span></span>

## <span data-ttu-id="6e487-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e487-104">SYNTAX</span></span>

### <span data-ttu-id="6e487-105">RemoveByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6e487-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e487-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="6e487-106">RemoveByResourceGroupId</span></span>
```
Remove-AzResourceGroup -Id <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e487-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e487-107">DESCRIPTION</span></span>
<span data-ttu-id="6e487-108">Il cmdlet **Remove-AzResourceGroup** rimuove un gruppo di risorse Azure e le relative risorse dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="6e487-108">The **Remove-AzResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="6e487-109">Per eliminare una risorsa, ma uscire dal gruppo risorse, usare il cmdlet Remove-AzResource.</span><span class="sxs-lookup"><span data-stu-id="6e487-109">To delete a resource, but leave the resource group, use the Remove-AzResource cmdlet.</span></span>

## <span data-ttu-id="6e487-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e487-110">EXAMPLES</span></span>

### <span data-ttu-id="6e487-111">Esempio 1: rimuovere un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6e487-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="6e487-112">Questo comando rimuove il gruppo di risorse ContosoRG01 dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6e487-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="6e487-113">Il cmdlet richiede la conferma e non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="6e487-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="6e487-114">Esempio 2: rimuovere un gruppo di risorse senza conferma</span><span class="sxs-lookup"><span data-stu-id="6e487-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzResourceGroup -Name "ContosoRG01" | Remove-AzResourceGroup -Force
```

<span data-ttu-id="6e487-115">Questo comando usa il cmdlet Get-AzResourceGroup per ottenere il gruppo di risorse ContosoRG01 e lo passa a **Remove-AzResourceGroup** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="6e487-115">This command uses the Get-AzResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzResourceGroup** by using the pipeline operator.</span></span> <span data-ttu-id="6e487-116">Il parametro *Force* Elimina il messaggio di conferma.</span><span class="sxs-lookup"><span data-stu-id="6e487-116">The *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="6e487-117">Esempio 3: rimuovere tutti i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="6e487-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Remove-AzResourceGroup
```

<span data-ttu-id="6e487-118">Questo comando usa il cmdlet **Get-AzResourceGroup** per ottenere tutti i gruppi di risorse, quindi li passa a **Remove-AzResourceGroup** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="6e487-118">This command uses the **Get-AzResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="6e487-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e487-119">PARAMETERS</span></span>

### <span data-ttu-id="6e487-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6e487-120">-ApiVersion</span></span>
<span data-ttu-id="6e487-121">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="6e487-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6e487-122">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6e487-122">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="6e487-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6e487-123">-AsJob</span></span>
<span data-ttu-id="6e487-124">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6e487-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6e487-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e487-125">-DefaultProfile</span></span>
<span data-ttu-id="6e487-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6e487-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e487-127">-Force</span><span class="sxs-lookup"><span data-stu-id="6e487-127">-Force</span></span>
<span data-ttu-id="6e487-128">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6e487-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6e487-129">-ID</span><span class="sxs-lookup"><span data-stu-id="6e487-129">-Id</span></span>
<span data-ttu-id="6e487-130">Specifica l'ID del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e487-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="6e487-131">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="6e487-131">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="6e487-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e487-132">-Name</span></span>
<span data-ttu-id="6e487-133">Specifica i nomi dei gruppi di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6e487-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="6e487-134">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="6e487-134">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="6e487-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="6e487-135">-Pre</span></span>
<span data-ttu-id="6e487-136">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="6e487-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6e487-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6e487-137">-Confirm</span></span>
<span data-ttu-id="6e487-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e487-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e487-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e487-139">-WhatIf</span></span>
<span data-ttu-id="6e487-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e487-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e487-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6e487-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e487-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e487-142">CommonParameters</span></span>
<span data-ttu-id="6e487-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e487-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e487-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e487-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e487-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e487-145">INPUTS</span></span>

### <span data-ttu-id="6e487-146">System. String</span><span class="sxs-lookup"><span data-stu-id="6e487-146">System.String</span></span>

## <span data-ttu-id="6e487-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e487-147">OUTPUTS</span></span>

### <span data-ttu-id="6e487-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6e487-148">System.Boolean</span></span>

## <span data-ttu-id="6e487-149">Note</span><span class="sxs-lookup"><span data-stu-id="6e487-149">NOTES</span></span>

## <span data-ttu-id="6e487-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e487-150">RELATED LINKS</span></span>

[<span data-ttu-id="6e487-151">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e487-151">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="6e487-152">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e487-152">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="6e487-153">Set-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e487-153">Set-AzResourceGroup</span></span>](./Set-AzResourceGroup.md)


