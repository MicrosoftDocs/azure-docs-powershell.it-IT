---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 880D321E-30F2-4CAE-B14A-5F6DD8E1DB99
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResourceGroup.md
ms.openlocfilehash: ce028e52d893372f4a668a278466d4cdc51655f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517996"
---
# <span data-ttu-id="6cef3-101">Remove-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6cef3-101">Remove-AzureRmResourceGroup</span></span>

## <span data-ttu-id="6cef3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6cef3-102">SYNOPSIS</span></span>
<span data-ttu-id="6cef3-103">Rimuove un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6cef3-103">Removes a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cef3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cef3-104">SYNTAX</span></span>

### <span data-ttu-id="6cef3-105">RemoveByResourceGroupName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6cef3-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzureRmResourceGroup [-Name] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6cef3-106">RemoveByResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="6cef3-106">RemoveByResourceGroupId</span></span>
```
Remove-AzureRmResourceGroup [-Id] <String> [-Force] [-AsJob] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6cef3-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cef3-107">DESCRIPTION</span></span>
<span data-ttu-id="6cef3-108">Il cmdlet **Remove-AzureRmResourceGroup** rimuove un gruppo di risorse Azure e le relative risorse dall'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="6cef3-108">The **Remove-AzureRmResourceGroup** cmdlet removes an Azure resource group and its resources from the current subscription.</span></span>
<span data-ttu-id="6cef3-109">Per eliminare una risorsa, ma uscire dal gruppo risorse, usare il cmdlet Remove-AzureRmResource.</span><span class="sxs-lookup"><span data-stu-id="6cef3-109">To delete a resource, but leave the resource group, use the Remove-AzureRmResource cmdlet.</span></span>

## <span data-ttu-id="6cef3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cef3-110">EXAMPLES</span></span>

### <span data-ttu-id="6cef3-111">Esempio 1: rimuovere un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="6cef3-111">Example 1: Remove a resource group</span></span>
```
PS C:\>Remove-AzureRmResourceGroup -Name "ContosoRG01"
```

<span data-ttu-id="6cef3-112">Questo comando rimuove il gruppo di risorse ContosoRG01 dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6cef3-112">This command removes the ContosoRG01 resource group from the subscription.</span></span>
<span data-ttu-id="6cef3-113">Il cmdlet richiede la conferma e non restituisce alcun output.</span><span class="sxs-lookup"><span data-stu-id="6cef3-113">The cmdlet prompts you for confirmation and returns no output.</span></span>

### <span data-ttu-id="6cef3-114">Esempio 2: rimuovere un gruppo di risorse senza conferma</span><span class="sxs-lookup"><span data-stu-id="6cef3-114">Example 2: Remove a resource group without confirmation</span></span>
```
PS C:\>Get-AzureRmResourceGroup -Name "ContosoRG01" | Remove-AzureRmResourceGroup -Verbose -Force
```

<span data-ttu-id="6cef3-115">Questo comando usa il cmdlet Get-AzureRmResourceGroup per ottenere il gruppo di risorse ContosoRG01 e lo passa a **Remove-AzureRmResourceGroup** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="6cef3-115">This command uses the Get-AzureRmResourceGroup cmdlet to get the resource group ContosoRG01, and then passes it to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>
<span data-ttu-id="6cef3-116">Il parametro comune *verbose* ottiene le informazioni sullo stato sull'operazione e il parametro *Force* Elimina il messaggio di conferma.</span><span class="sxs-lookup"><span data-stu-id="6cef3-116">The *Verbose* common parameter gets status information about the operation, and the *Force* parameter suppresses the confirmation prompt.</span></span>

### <span data-ttu-id="6cef3-117">Esempio 3: rimuovere tutti i gruppi di risorse</span><span class="sxs-lookup"><span data-stu-id="6cef3-117">Example 3: Remove all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Remove-AzureRmResourceGroup
```

<span data-ttu-id="6cef3-118">Questo comando usa il cmdlet **Get-AzureRmResourceGroup** per ottenere tutti i gruppi di risorse, quindi li passa a **Remove-AzureRmResourceGroup** usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="6cef3-118">This command uses the **Get-AzureRmResourceGroup** cmdlet to get all resource groups, and then passes them to **Remove-AzureRmResourceGroup** by using the pipeline operator.</span></span>

## <span data-ttu-id="6cef3-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6cef3-119">PARAMETERS</span></span>

### <span data-ttu-id="6cef3-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6cef3-120">-ApiVersion</span></span>
<span data-ttu-id="6cef3-121">Specifica la versione dell'API supportata dal provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="6cef3-121">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="6cef3-122">Puoi specificare una versione diversa rispetto alla versione predefinita.</span><span class="sxs-lookup"><span data-stu-id="6cef3-122">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cef3-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6cef3-123">-AsJob</span></span>
<span data-ttu-id="6cef3-124">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6cef3-124">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cef3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cef3-125">-DefaultProfile</span></span>
<span data-ttu-id="6cef3-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6cef3-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cef3-127">-Force</span><span class="sxs-lookup"><span data-stu-id="6cef3-127">-Force</span></span>
<span data-ttu-id="6cef3-128">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6cef3-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cef3-129">-ID</span><span class="sxs-lookup"><span data-stu-id="6cef3-129">-Id</span></span>
<span data-ttu-id="6cef3-130">Specifica l'ID del gruppo di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6cef3-130">Specifies the ID of resource group to remove.</span></span>
<span data-ttu-id="6cef3-131">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="6cef3-131">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cef3-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="6cef3-132">-Name</span></span>
<span data-ttu-id="6cef3-133">Specifica i nomi dei gruppi di risorse da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6cef3-133">Specifies the names of resource groups to remove.</span></span>
<span data-ttu-id="6cef3-134">I caratteri jolly non sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="6cef3-134">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceGroupName
Aliases: ResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cef3-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="6cef3-135">-Pre</span></span>
<span data-ttu-id="6cef3-136">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="6cef3-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cef3-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6cef3-137">-Confirm</span></span>
<span data-ttu-id="6cef3-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6cef3-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cef3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6cef3-139">-WhatIf</span></span>
<span data-ttu-id="6cef3-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cef3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6cef3-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6cef3-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cef3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cef3-142">CommonParameters</span></span>
<span data-ttu-id="6cef3-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cef3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cef3-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cef3-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cef3-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6cef3-145">INPUTS</span></span>

### <span data-ttu-id="6cef3-146">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6cef3-146">None</span></span>

## <span data-ttu-id="6cef3-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cef3-147">OUTPUTS</span></span>

### <span data-ttu-id="6cef3-148">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6cef3-148">None</span></span>

## <span data-ttu-id="6cef3-149">Note</span><span class="sxs-lookup"><span data-stu-id="6cef3-149">NOTES</span></span>

## <span data-ttu-id="6cef3-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cef3-150">RELATED LINKS</span></span>

[<span data-ttu-id="6cef3-151">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6cef3-151">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="6cef3-152">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6cef3-152">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="6cef3-153">Set-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6cef3-153">Set-AzureRmResourceGroup</span></span>](./Set-AzureRmResourceGroup.md)


